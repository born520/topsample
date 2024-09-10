document.addEventListener('DOMContentLoaded', function() {
    const content = document.getElementById('content');
    const originalUrl = content.dataset.originalUrl;

    if (originalUrl) {
        fetch(originalUrl)
            .then(response => response.text())
            .then(html => {
                const parser = new DOMParser();
                const doc = parser.parseFromString(html, 'text/html');
                content.innerHTML = doc.body.innerHTML;
            })
            .catch(error => {
                console.error('콘텐츠를 불러오는 중 오류가 발생했습니다:', error);
                content.innerHTML = '콘텐츠를 불러오는 데 실패했습니다.';
            });
    }
});
