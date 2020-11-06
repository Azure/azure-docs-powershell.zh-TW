---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 27FF1B7D-E103-4504-AD09-8D3A8BCA8B75
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementuserssourl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUserSsoUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUserSsoUrl.md
ms.openlocfilehash: 2a7a4d602b8e316377496af8ccb9c119338a5c99
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93611602"
---
# <span data-ttu-id="cb77e-101">Get-AzApiManagementUserSsoUrl</span><span class="sxs-lookup"><span data-stu-id="cb77e-101">Get-AzApiManagementUserSsoUrl</span></span>

## <span data-ttu-id="cb77e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cb77e-102">SYNOPSIS</span></span>
<span data-ttu-id="cb77e-103">為使用者產生 SSO URL。</span><span class="sxs-lookup"><span data-stu-id="cb77e-103">Generates an SSO URL for a user.</span></span>

## <span data-ttu-id="cb77e-104">句法</span><span class="sxs-lookup"><span data-stu-id="cb77e-104">SYNTAX</span></span>

```
Get-AzApiManagementUserSsoUrl -Context <PsApiManagementContext> -UserId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb77e-105">說明</span><span class="sxs-lookup"><span data-stu-id="cb77e-105">DESCRIPTION</span></span>
<span data-ttu-id="cb77e-106">**AzApiManagementUserSsoUrl** Cmdlet 會為使用者產生單一登入 (SSO) URL。</span><span class="sxs-lookup"><span data-stu-id="cb77e-106">The **Get-AzApiManagementUserSsoUrl** cmdlet generates a single sign-on (SSO) URL for a user.</span></span>

## <span data-ttu-id="cb77e-107">示例</span><span class="sxs-lookup"><span data-stu-id="cb77e-107">EXAMPLES</span></span>

### <span data-ttu-id="cb77e-108">範例1：取得使用者的 SSO URL</span><span class="sxs-lookup"><span data-stu-id="cb77e-108">Example 1: Get a user's SSO URL</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUserSsoUrl -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="cb77e-109">這個命令會取得使用者的 SSO URL。</span><span class="sxs-lookup"><span data-stu-id="cb77e-109">This command gets a user's SSO URL.</span></span>

## <span data-ttu-id="cb77e-110">參數</span><span class="sxs-lookup"><span data-stu-id="cb77e-110">PARAMETERS</span></span>

### <span data-ttu-id="cb77e-111">-內容</span><span class="sxs-lookup"><span data-stu-id="cb77e-111">-Context</span></span>
<span data-ttu-id="cb77e-112">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="cb77e-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="cb77e-113">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="cb77e-113">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb77e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb77e-114">-DefaultProfile</span></span>
<span data-ttu-id="cb77e-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cb77e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb77e-116">-UserId</span><span class="sxs-lookup"><span data-stu-id="cb77e-116">-UserId</span></span>
<span data-ttu-id="cb77e-117">指定使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="cb77e-117">Specifies a user ID.</span></span>
<span data-ttu-id="cb77e-118">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="cb77e-118">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb77e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb77e-119">CommonParameters</span></span>
<span data-ttu-id="cb77e-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cb77e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb77e-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cb77e-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb77e-122">輸入</span><span class="sxs-lookup"><span data-stu-id="cb77e-122">INPUTS</span></span>

### <span data-ttu-id="cb77e-123">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="cb77e-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="cb77e-124">System.object</span><span class="sxs-lookup"><span data-stu-id="cb77e-124">System.String</span></span>

## <span data-ttu-id="cb77e-125">輸出</span><span class="sxs-lookup"><span data-stu-id="cb77e-125">OUTPUTS</span></span>

### <span data-ttu-id="cb77e-126">System.object</span><span class="sxs-lookup"><span data-stu-id="cb77e-126">System.String</span></span>

## <span data-ttu-id="cb77e-127">筆記</span><span class="sxs-lookup"><span data-stu-id="cb77e-127">NOTES</span></span>

## <span data-ttu-id="cb77e-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="cb77e-128">RELATED LINKS</span></span>

[<span data-ttu-id="cb77e-129">AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="cb77e-129">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)


