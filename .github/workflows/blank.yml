    <script>
        // Tab functionality
        function openTab(evt, tabName) {
            // Declare all variables
            var i, tabcontent, tablinks;

            // Get all elements with class="tabcontent" and hide them
            tabcontent = document.getElementsByClassName("tabcontent");
            for (i = 0; i < tabcontent.length; i++) {
                tabcontent[i].classList.remove("active");
            }

            // Get all elements with class="tablinks" and remove the class "active"
            tablinks = document.getElementsByClassName("tablinks");
            for (i = 0; i < tablinks.length; i++) {
                tablinks[i].classList.remove("active");
            }

            // Show the current tab, and add an "active" class to the button that opened the tab
            document.getElementById(tabName).classList.add("active");
            evt.currentTarget.classList.add("active");

            // Smooth scroll to top
            window.scrollTo({ top: 0, behavior: 'smooth' });
        }

        // Form submission handler
        function handleSubmit(e) {
            e.preventDefault();
            alert('Thank you for your message! We will get back to you soon.');
            e.target.reset();
        }

        // Remove loader when page loads
        window.addEventListener('load', function () {
            setTimeout(function () {
                document.getElementById('loader').classList.add('hidden');
            }, 500);
        });

        // Video error handling
        document.getElementById('bg-video').addEventListener('error', function () {
            this.style.display = 'none';
            console.log('Video failed to load, using fallback background');
        });
    </script>
</body>
</html>
