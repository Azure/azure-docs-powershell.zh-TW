---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 27FF1B7D-E103-4504-AD09-8D3A8BCA8B75
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementuserssourl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUserSsoUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUserSsoUrl.md
ms.openlocfilehash: be30497c444d90b9239b5dc3dcd351fbe9a63f0b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94137907"
---
# <span data-ttu-id="68c36-101">Get-AzApiManagementUserSsoUrl</span><span class="sxs-lookup"><span data-stu-id="68c36-101">Get-AzApiManagementUserSsoUrl</span></span>

## <span data-ttu-id="68c36-102">摘要</span><span class="sxs-lookup"><span data-stu-id="68c36-102">SYNOPSIS</span></span>
<span data-ttu-id="68c36-103">為使用者產生 SSO URL。</span><span class="sxs-lookup"><span data-stu-id="68c36-103">Generates an SSO URL for a user.</span></span>

## <span data-ttu-id="68c36-104">句法</span><span class="sxs-lookup"><span data-stu-id="68c36-104">SYNTAX</span></span>

```
Get-AzApiManagementUserSsoUrl -Context <PsApiManagementContext> -UserId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="68c36-105">說明</span><span class="sxs-lookup"><span data-stu-id="68c36-105">DESCRIPTION</span></span>
<span data-ttu-id="68c36-106">**AzApiManagementUserSsoUrl** Cmdlet 會為使用者產生單一登入 (SSO) URL。</span><span class="sxs-lookup"><span data-stu-id="68c36-106">The **Get-AzApiManagementUserSsoUrl** cmdlet generates a single sign-on (SSO) URL for a user.</span></span>

## <span data-ttu-id="68c36-107">示例</span><span class="sxs-lookup"><span data-stu-id="68c36-107">EXAMPLES</span></span>

### <span data-ttu-id="68c36-108">範例1：取得使用者的 SSO URL</span><span class="sxs-lookup"><span data-stu-id="68c36-108">Example 1: Get a user's SSO URL</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUserSsoUrl -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="68c36-109">這個命令會取得使用者的 SSO URL。</span><span class="sxs-lookup"><span data-stu-id="68c36-109">This command gets a user's SSO URL.</span></span>

## <span data-ttu-id="68c36-110">參數</span><span class="sxs-lookup"><span data-stu-id="68c36-110">PARAMETERS</span></span>

### <span data-ttu-id="68c36-111">-內容</span><span class="sxs-lookup"><span data-stu-id="68c36-111">-Context</span></span>
<span data-ttu-id="68c36-112">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="68c36-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="68c36-113">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="68c36-113">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="68c36-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68c36-114">-DefaultProfile</span></span>
<span data-ttu-id="68c36-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="68c36-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="68c36-116">-UserId</span><span class="sxs-lookup"><span data-stu-id="68c36-116">-UserId</span></span>
<span data-ttu-id="68c36-117">指定使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="68c36-117">Specifies a user ID.</span></span>
<span data-ttu-id="68c36-118">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="68c36-118">This parameter is required.</span></span>

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

### <span data-ttu-id="68c36-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68c36-119">CommonParameters</span></span>
<span data-ttu-id="68c36-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="68c36-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68c36-121">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="68c36-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68c36-122">輸入</span><span class="sxs-lookup"><span data-stu-id="68c36-122">INPUTS</span></span>

### <span data-ttu-id="68c36-123">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="68c36-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="68c36-124">System.object</span><span class="sxs-lookup"><span data-stu-id="68c36-124">System.String</span></span>

## <span data-ttu-id="68c36-125">輸出</span><span class="sxs-lookup"><span data-stu-id="68c36-125">OUTPUTS</span></span>

### <span data-ttu-id="68c36-126">System.object</span><span class="sxs-lookup"><span data-stu-id="68c36-126">System.String</span></span>

## <span data-ttu-id="68c36-127">筆記</span><span class="sxs-lookup"><span data-stu-id="68c36-127">NOTES</span></span>

## <span data-ttu-id="68c36-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="68c36-128">RELATED LINKS</span></span>

[<span data-ttu-id="68c36-129">AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="68c36-129">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)


