<template>
  <div class="flex items-center justify-center p-4">
    <div
      class="w-full max-w-5xl rounded-2xl border border-gray-200 overflow-hidden"
    >
      <div class="grid md:grid-cols-2 relative">
        <!-- Contact Info Section -->
        <div
          class="p-8 md:p-12 border-b md:border-b-0 md:border-r border-gray-200 relative"
        >
          <div
            class="absolute top-0 left-0 w-full h-1 bg-gradient-to-r from-primary to-primary-light"
          ></div>

          <h2 class="text-2xl font-bold text-gray-800 mb-6">Get in Touch</h2>

          <div class="space-y-8">
            <div class="flex items-start space-x-4">
              <div class="bg-white p-3 rounded-full border border-gray-200">
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  width="24"
                  height="24"
                  viewBox="0 0 24 24"
                  fill="none"
                  stroke="currentColor"
                  stroke-width="2"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  class="text-primary"
                >
                  <path
                    d="M22 16.92v3a2 2 0 0 1-2.18 2 19.79 19.79 0 0 1-8.63-3.07 19.5 19.5 0 0 1-6-6 19.79 19.79 0 0 1-3.07-8.67A2 2 0 0 1 4.11 2h3a2 2 0 0 1 2 1.72 12.84 12.84 0 0 0 .7 2.81 2 2 0 0 1-.45 2.11L8.09 9.91a16 16 0 0 0 6 6l1.27-1.27a2 2 0 0 1 2.11-.45 12.84 12.84 0 0 0 2.81.7A2 2 0 0 1 22 16.92z"
                  ></path>
                </svg>
              </div>
              <div>
                <h3 class="font-semibold text-gray-700">Phone</h3>
                <p class="text-gray-600 mt-1">{{ phone }}</p>
                <p class="text-gray-500 text-sm mt-1">
                  Mon-Fri from 8am to 6pm
                </p>
              </div>
            </div>

            <div class="flex items-start space-x-4">
              <div class="bg-white p-3 rounded-full border border-gray-200">
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  width="24"
                  height="24"
                  viewBox="0 0 24 24"
                  fill="none"
                  stroke="currentColor"
                  stroke-width="2"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  class="text-primary"
                >
                  <rect width="20" height="16" x="2" y="4" rx="2"></rect>
                  <path d="m22 7-8.97 5.7a1.94 1.94 0 0 1-2.06 0L2 7"></path>
                </svg>
              </div>
              <div>
                <h3 class="font-semibold text-gray-700">Email</h3>
                <p class="text-gray-600 mt-1">{{ email }}</p>
                <p class="text-gray-500 text-sm mt-1">
                  We'll respond within 24 hours
                </p>
              </div>
            </div>

            <div class="flex items-start space-x-4">
              <div
                class="bg-white p-3 rounded-full border border-gray-200 z-20"
              >
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  width="24"
                  height="24"
                  viewBox="0 0 24 24"
                  fill="none"
                  stroke="currentColor"
                  stroke-width="2"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  class="text-primary"
                >
                  <path
                    d="M20 10c0 6-8 12-8 12s-8-6-8-12a8 8 0 0 1 16 0Z"
                  ></path>
                  <circle cx="12" cy="10" r="3"></circle>
                </svg>
              </div>
              <div>
                <h3 class="font-semibold text-gray-700">Office</h3>
                <p class="text-gray-600 mt-1">Dembel City Center</p>
                <p class="text-gray-500 text-sm mt-1">
                  Africa Ave, Addis Ababa
                </p>
              </div>
            </div>
          </div>

          <div class="mt-12">
            <h3 class="font-semibold text-gray-700 mb-4">Connect with us</h3>
            <div class="flex space-x-4">
              <a
                href="#"
                class="bg-white p-3 rounded-full border border-gray-200 hover:border-primary transition-colors"
              >
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  width="20"
                  height="20"
                  viewBox="0 0 24 24"
                  fill="none"
                  stroke="currentColor"
                  stroke-width="2"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  class="text-primary"
                >
                  <path
                    d="M18 2h-3a5 5 0 0 0-5 5v3H7v4h3v8h4v-8h3l1-4h-4V7a1 1 0 0 1 1-1h3z"
                  ></path>
                </svg>
              </a>
              <a
                href="#"
                class="bg-white p-3 rounded-full border border-gray-200 hover:border-primary transition-colors"
              >
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  width="20"
                  height="20"
                  viewBox="0 0 24 24"
                  fill="none"
                  stroke="currentColor"
                  stroke-width="2"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  class="text-primary"
                >
                  <path
                    d="M22 4s-.7 2.1-2 3.4c1.6 10-9.4 17.3-18 11.6 2.2.1 4.4-.6 6-2C3 15.5.5 9.6 3 5c2.2 2.6 5.6 4.1 9 4-.9-4.2 4-6.6 7-3.8 1.1 0 3-1.2 3-1.2z"
                  ></path>
                </svg>
              </a>
              <a
                href="#"
                class="bg-white p-3 rounded-full border border-gray-200 hover:border-primary transition-colors"
              >
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  width="20"
                  height="20"
                  viewBox="0 0 24 24"
                  fill="none"
                  stroke="currentColor"
                  stroke-width="2"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  class="text-primary"
                >
                  <rect width="20" height="20" x="2" y="2" rx="5" ry="5"></rect>
                  <path
                    d="M16 11.37A4 4 0 1 1 12.63 8 4 4 0 0 1 16 11.37z"
                  ></path>
                  <line x1="17.5" x2="17.51" y1="6.5" y2="6.5"></line>
                </svg>
              </a>
              <a
                href="#"
                class="bg-white p-3 rounded-full border border-gray-200 hover:border-primary transition-colors"
              >
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  width="20"
                  height="20"
                  viewBox="0 0 24 24"
                  fill="none"
                  stroke="currentColor"
                  stroke-width="2"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  class="text-primary"
                >
                  <path
                    d="M16 8a6 6 0 0 1 6 6v7h-4v-7a2 2 0 0 0-2-2 2 2 0 0 0-2 2v7h-4v-7a6 6 0 0 1 6-6z"
                  ></path>
                  <rect width="4" height="12" x="2" y="9"></rect>
                  <circle cx="4" cy="4" r="2"></circle>
                </svg>
              </a>
            </div>
          </div>
        </div>

        <!-- Contact Form Section -->
        <div class="p-8 md:p-12 relative">
          <div
            class="absolute top-0 right-0 w-1 h-full bg-gradient-to-b from-primary to-primary-light hidden md:block"
          ></div>

          <h2 class="text-2xl font-bold text-gray-800 mb-6">Send a Message</h2>

          <form @submit.prevent="submitForm" class="space-y-6">
            <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
              <div>
                <label
                  for="firstName"
                  class="block text-sm font-medium text-gray-700 mb-1"
                  >First Name</label
                >
                <div class="relative">
                  <input
                    type="text"
                    id="firstName"
                    v-model="form.firstName"
                    class="w-full px-4 py-3 border border-gray-200 rounded-lg focus:ring-1 focus:ring-primary outline-none transition-colors"
                    :class="{ 'border-red-300': errors.firstName }"
                  />
                  <p v-if="errors.firstName" class="text-red-500 text-xs mt-1">
                    {{ errors.firstName }}
                  </p>
                </div>
              </div>

              <div>
                <label
                  for="lastName"
                  class="block text-sm font-medium text-gray-700 mb-1"
                  >Last Name</label
                >
                <div class="relative">
                  <input
                    type="text"
                    id="lastName"
                    v-model="form.lastName"
                    class="w-full px-4 py-3 border border-gray-200 rounded-lg focus:ring-1 focus:ring-primary outline-none transition-colors"
                    :class="{ 'border-red-300': errors.lastName }"
                  />
                  <p v-if="errors.lastName" class="text-red-500 text-xs mt-1">
                    {{ errors.lastName }}
                  </p>
                </div>
              </div>
            </div>

            <div>
              <label
                for="email"
                class="block text-sm font-medium text-gray-700 mb-1"
                >Email Address</label
              >
              <div class="relative">
                <input
                  type="email"
                  id="email"
                  v-model="form.email"
                  class="w-full px-4 py-3 border border-gray-200 rounded-lg focus:ring-1 focus:ring-primary outline-none transition-colors"
                  :class="{ 'border-red-300': errors.email }"
                />
                <p v-if="errors.email" class="text-red-500 text-xs mt-1">
                  {{ errors.email }}
                </p>
              </div>
            </div>

            <div>
              <label
                for="subject"
                class="block text-sm font-medium text-gray-700 mb-1"
                >Subject</label
              >
              <div class="relative">
                <select
                  id="subject"
                  v-model="form.subject"
                  class="w-full px-4 py-3 border border-gray-200 rounded-lg focus:ring-1 focus:ring-primary outline-none transition-colors appearance-none"
                  :class="{ 'border-red-300': errors.subject }"
                >
                  <option value="" disabled>Please select a subject</option>
                  <option value="general">General Inquiry</option>
                  <option value="support">Technical Support</option>
                  <option value="billing">Billing Question</option>
                  <option value="partnership">Partnership Opportunity</option>
                </select>
                <div
                  class="absolute right-4 top-1/2 transform -translate-y-1/2 pointer-events-none"
                >
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    width="16"
                    height="16"
                    viewBox="0 0 24 24"
                    fill="none"
                    stroke="currentColor"
                    stroke-width="2"
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    class="text-gray-400"
                  >
                    <path d="m6 9 6 6 6-6"></path>
                  </svg>
                </div>
                <p v-if="errors.subject" class="text-red-500 text-xs mt-1">
                  {{ errors.subject }}
                </p>
              </div>
            </div>

            <div>
              <label
                for="message"
                class="block text-sm font-medium text-gray-700 mb-1"
                >Message</label
              >
              <div class="relative">
                <textarea
                  id="message"
                  v-model="form.message"
                  rows="4"
                  class="w-full px-4 py-3 border border-gray-200 rounded-lg focus:ring-1 focus:ring-primary outline-none transition-colors resize-none"
                  :class="{ 'border-red-300': errors.message }"
                ></textarea>
                <p v-if="errors.message" class="text-red-500 text-xs mt-1">
                  {{ errors.message }}
                </p>
              </div>
            </div>

            <Button type="submit" :disabled="isSubmitting" class="">
              <div class="flex items-center justify-center">
                <svg
                  v-if="isSubmitting"
                  class="animate-spin -ml-1 mr-2 h-4 w-4 text-white"
                  xmlns="http://www.w3.org/2000/svg"
                  fill="none"
                  viewBox="0 0 24 24"
                >
                  <circle
                    class="opacity-25"
                    cx="12"
                    cy="12"
                    r="10"
                    stroke="currentColor"
                    stroke-width="4"
                  ></circle>
                  <path
                    class="opacity-75"
                    fill="currentColor"
                    d="M4 12a8 8 0 018-8V0C5.373 0 0 5.373 0 12h4zm2 5.291A7.962 7.962 0 014 12H0c0 3.042 1.135 5.824 3 7.938l3-2.647z"
                  ></path>
                </svg>
                <span>{{ isSubmitting ? "Sending..." : "Send Message" }}</span>
              </div>
            </Button>

            <div
              v-if="formSubmitted"
              class="bg-green-50 border border-green-200 text-green-700 px-4 py-3 rounded-lg"
            >
              Thank you for your message! We'll get back to you soon.
            </div>
          </form>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
const { phone, email } = useCompanyInfo();
const form = reactive({
  firstName: "",
  lastName: "",
  email: "",
  subject: "",
  message: "",
  privacy: false,
});

const errors = reactive({
  firstName: "",
  lastName: "",
  email: "",
  subject: "",
  message: "",
  privacy: "",
});

const isSubmitting = ref(false);
const formSubmitted = ref(false);

const validateForm = () => {
  let isValid = true;

  // Reset errors
  Object.keys(errors).forEach((key) => {
    errors[key] = "";
  });

  if (!form.firstName.trim()) {
    errors.firstName = "First name is required";
    isValid = false;
  }

  if (!form.lastName.trim()) {
    errors.lastName = "Last name is required";
    isValid = false;
  }

  if (!form.email.trim()) {
    errors.email = "Email is required";
    isValid = false;
  } else if (!/^\S+@\S+\.\S+$/.test(form.email)) {
    errors.email = "Please enter a valid email address";
    isValid = false;
  }

  if (!form.subject) {
    errors.subject = "Please select a subject";
    isValid = false;
  }

  if (!form.message.trim()) {
    errors.message = "Message is required";
    isValid = false;
  } else if (form.message.length < 10) {
    errors.message = "Message must be at least 10 characters";
    isValid = false;
  }

  if (!form.privacy) {
    errors.privacy = "You must agree to the privacy policy";
    isValid = false;
  }

  return isValid;
};

const submitForm = async () => {
  if (!validateForm()) return;

  isSubmitting.value = true;

  try {
    // Simulate API call
    await new Promise((resolve) => setTimeout(resolve, 1500));

    // Reset form after successful submission
    Object.keys(form).forEach((key) => {
      if (key === "privacy") {
        form[key] = false;
      } else {
        form[key] = "";
      }
    });

    formSubmitted.value = true;

    // Hide success message after 5 seconds
    setTimeout(() => {
      formSubmitted.value = false;
    }, 5000);
  } catch (error) {
    console.error("Error submitting form:", error);
  } finally {
    isSubmitting.value = false;
  }
};
</script>

<style scoped>
/* Optional: Add custom styles here if needed */
</style>
