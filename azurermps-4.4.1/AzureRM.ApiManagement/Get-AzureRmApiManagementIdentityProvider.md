---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementIdentityProvider.md
ms.openlocfilehash: 2b38728f90de4639bf3e125f226ae2b40527ca45
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450136"
---
# <span data-ttu-id="91aef-101">Get-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="91aef-101">Get-AzureRmApiManagementIdentityProvider</span></span>

## <span data-ttu-id="91aef-102">摘要</span><span class="sxs-lookup"><span data-stu-id="91aef-102">SYNOPSIS</span></span>
<span data-ttu-id="91aef-103">取得身分識別提供者設定的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="91aef-103">Get the identity provider configuration details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="91aef-104">句法</span><span class="sxs-lookup"><span data-stu-id="91aef-104">SYNTAX</span></span>

### <span data-ttu-id="91aef-105">AllIdentityProviders (預設) </span><span class="sxs-lookup"><span data-stu-id="91aef-105">AllIdentityProviders (Default)</span></span>
```
Get-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91aef-106">IdentityProviderByType</span><span class="sxs-lookup"><span data-stu-id="91aef-106">IdentityProviderByType</span></span>
```
Get-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91aef-107">說明</span><span class="sxs-lookup"><span data-stu-id="91aef-107">DESCRIPTION</span></span>
<span data-ttu-id="91aef-108">取得身分識別提供者設定的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="91aef-108">Get the identity provider configuration details.</span></span>

## <span data-ttu-id="91aef-109">示例</span><span class="sxs-lookup"><span data-stu-id="91aef-109">EXAMPLES</span></span>

### <span data-ttu-id="91aef-110">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="91aef-110">--------------------------  Example 1  --------------------------</span></span>
<span data-ttu-id="91aef-111">@ {段落 = PS C： \\ \> }</span><span class="sxs-lookup"><span data-stu-id="91aef-111">@{paragraph=PS C:\\\>}</span></span>







```
Get-AzureRmApiManagementIdentityProvider -Context $context
```

<span data-ttu-id="91aef-112">取得服務上的所有身分識別提供者設定。</span><span class="sxs-lookup"><span data-stu-id="91aef-112">Get all the identity provider Configuration on the service.</span></span>

### <span data-ttu-id="91aef-113">--------------------------範例 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="91aef-113">--------------------------  Example 2  --------------------------</span></span>
<span data-ttu-id="91aef-114">@ {段落 = PS C： \\ \> }</span><span class="sxs-lookup"><span data-stu-id="91aef-114">@{paragraph=PS C:\\\>}</span></span>







```
Get-AzureRmApiManagementIdentityProvider -Context $context -Type Aad
```

<span data-ttu-id="91aef-115">取得 Azure Active Directory 的身分識別提供者設定。</span><span class="sxs-lookup"><span data-stu-id="91aef-115">Gets the Identity Provider Configuration of Azure Active Directory.</span></span>

## <span data-ttu-id="91aef-116">參數</span><span class="sxs-lookup"><span data-stu-id="91aef-116">PARAMETERS</span></span>

### <span data-ttu-id="91aef-117">-內容</span><span class="sxs-lookup"><span data-stu-id="91aef-117">-Context</span></span>
<span data-ttu-id="91aef-118">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="91aef-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="91aef-119">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="91aef-119">This parameter is required.</span></span>

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

### <span data-ttu-id="91aef-120">-類型</span><span class="sxs-lookup"><span data-stu-id="91aef-120">-Type</span></span>
<span data-ttu-id="91aef-121">身分識別提供者的識別碼。</span><span class="sxs-lookup"><span data-stu-id="91aef-121">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="91aef-122">如果已指定，將會嘗試透過識別碼尋找身分識別提供者設定。</span><span class="sxs-lookup"><span data-stu-id="91aef-122">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="91aef-123">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="91aef-123">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType
Parameter Sets: IdentityProviderByType
Aliases: 
Accepted values: Facebook, Google, Microsoft, Twitter, Aad

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91aef-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91aef-124">-DefaultProfile</span></span>
<span data-ttu-id="91aef-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="91aef-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91aef-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91aef-126">CommonParameters</span></span>
<span data-ttu-id="91aef-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="91aef-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91aef-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="91aef-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91aef-129">輸入</span><span class="sxs-lookup"><span data-stu-id="91aef-129">INPUTS</span></span>

## <span data-ttu-id="91aef-130">輸出</span><span class="sxs-lookup"><span data-stu-id="91aef-130">OUTPUTS</span></span>

### <span data-ttu-id="91aef-131">IList<ApiManagement. ServiceManagement. PsApiManagementIdentityProvider]></span><span class="sxs-lookup"><span data-stu-id="91aef-131">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider></span></span>

### <span data-ttu-id="91aef-132">ServiceManagement. PsApiManagementIdentityProvider （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="91aef-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="91aef-133">筆記</span><span class="sxs-lookup"><span data-stu-id="91aef-133">NOTES</span></span>

## <span data-ttu-id="91aef-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="91aef-134">RELATED LINKS</span></span>

