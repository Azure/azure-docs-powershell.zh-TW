---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 27FF1B7D-E103-4504-AD09-8D3A8BCA8B75
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUserSsoUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUserSsoUrl.md
ms.openlocfilehash: a13d37100e553d8d56cf5b040a796adabe08b7d9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450126"
---
# <span data-ttu-id="9ce4e-101">Get-AzureRmApiManagementUserSsoUrl</span><span class="sxs-lookup"><span data-stu-id="9ce4e-101">Get-AzureRmApiManagementUserSsoUrl</span></span>

## <span data-ttu-id="9ce4e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9ce4e-102">SYNOPSIS</span></span>
<span data-ttu-id="9ce4e-103">為使用者產生 SSO URL。</span><span class="sxs-lookup"><span data-stu-id="9ce4e-103">Generates an SSO URL for a user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9ce4e-104">句法</span><span class="sxs-lookup"><span data-stu-id="9ce4e-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementUserSsoUrl -Context <PsApiManagementContext> -UserId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9ce4e-105">說明</span><span class="sxs-lookup"><span data-stu-id="9ce4e-105">DESCRIPTION</span></span>
<span data-ttu-id="9ce4e-106">**AzureRmApiManagementUserSsoUrl** Cmdlet 會為使用者產生單一登入 (SSO) URL。</span><span class="sxs-lookup"><span data-stu-id="9ce4e-106">The **Get-AzureRmApiManagementUserSsoUrl** cmdlet generates a single sign-on (SSO) URL for a user.</span></span>

## <span data-ttu-id="9ce4e-107">示例</span><span class="sxs-lookup"><span data-stu-id="9ce4e-107">EXAMPLES</span></span>

### <span data-ttu-id="9ce4e-108">範例1：取得使用者的 SSO URL</span><span class="sxs-lookup"><span data-stu-id="9ce4e-108">Example 1: Get a user's SSO URL</span></span>
```
PS C:\>Get-AzureRmApiManagementUserSsoUrl -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="9ce4e-109">這個命令會取得使用者的 SSO URL。</span><span class="sxs-lookup"><span data-stu-id="9ce4e-109">This command gets a user's SSO URL.</span></span>

## <span data-ttu-id="9ce4e-110">參數</span><span class="sxs-lookup"><span data-stu-id="9ce4e-110">PARAMETERS</span></span>

### <span data-ttu-id="9ce4e-111">-內容</span><span class="sxs-lookup"><span data-stu-id="9ce4e-111">-Context</span></span>
<span data-ttu-id="9ce4e-112">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="9ce4e-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="9ce4e-113">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="9ce4e-113">This parameter is required.</span></span>

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

### <span data-ttu-id="9ce4e-114">-UserId</span><span class="sxs-lookup"><span data-stu-id="9ce4e-114">-UserId</span></span>
<span data-ttu-id="9ce4e-115">指定使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="9ce4e-115">Specifies a user ID.</span></span>
<span data-ttu-id="9ce4e-116">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="9ce4e-116">This parameter is required.</span></span>

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

### <span data-ttu-id="9ce4e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ce4e-117">-DefaultProfile</span></span>
<span data-ttu-id="9ce4e-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9ce4e-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ce4e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ce4e-119">CommonParameters</span></span>
<span data-ttu-id="9ce4e-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9ce4e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ce4e-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9ce4e-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ce4e-122">輸入</span><span class="sxs-lookup"><span data-stu-id="9ce4e-122">INPUTS</span></span>

## <span data-ttu-id="9ce4e-123">輸出</span><span class="sxs-lookup"><span data-stu-id="9ce4e-123">OUTPUTS</span></span>

### <span data-ttu-id="9ce4e-124">字串</span><span class="sxs-lookup"><span data-stu-id="9ce4e-124">string</span></span>

## <span data-ttu-id="9ce4e-125">筆記</span><span class="sxs-lookup"><span data-stu-id="9ce4e-125">NOTES</span></span>

## <span data-ttu-id="9ce4e-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="9ce4e-126">RELATED LINKS</span></span>

[<span data-ttu-id="9ce4e-127">AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="9ce4e-127">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)


