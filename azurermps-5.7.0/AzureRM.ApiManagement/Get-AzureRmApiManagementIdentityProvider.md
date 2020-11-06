---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementIdentityProvider.md
ms.openlocfilehash: e25e3bfad6c40b136c3cbaa65999b8118e0abd11
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452283"
---
# <span data-ttu-id="07724-101">Get-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="07724-101">Get-AzureRmApiManagementIdentityProvider</span></span>

## <span data-ttu-id="07724-102">摘要</span><span class="sxs-lookup"><span data-stu-id="07724-102">SYNOPSIS</span></span>
<span data-ttu-id="07724-103">取得身分識別提供者設定的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="07724-103">Get the identity provider configuration details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="07724-104">句法</span><span class="sxs-lookup"><span data-stu-id="07724-104">SYNTAX</span></span>

### <span data-ttu-id="07724-105">AllIdentityProviders (預設) </span><span class="sxs-lookup"><span data-stu-id="07724-105">AllIdentityProviders (Default)</span></span>
```
Get-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="07724-106">IdentityProviderByType</span><span class="sxs-lookup"><span data-stu-id="07724-106">IdentityProviderByType</span></span>
```
Get-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07724-107">說明</span><span class="sxs-lookup"><span data-stu-id="07724-107">DESCRIPTION</span></span>
<span data-ttu-id="07724-108">取得身分識別提供者設定的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="07724-108">Get the identity provider configuration details.</span></span>

## <span data-ttu-id="07724-109">示例</span><span class="sxs-lookup"><span data-stu-id="07724-109">EXAMPLES</span></span>

### <span data-ttu-id="07724-110">範例1：取得所有身分識別提供者</span><span class="sxs-lookup"><span data-stu-id="07724-110">Example 1: Get all Identity Providers</span></span>

```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementIdentityProvider -Context $apimContext
```

<span data-ttu-id="07724-111">取得服務上的所有身分識別提供者設定。</span><span class="sxs-lookup"><span data-stu-id="07724-111">Get all the identity provider Configuration on the service.</span></span>

### <span data-ttu-id="07724-112">取得 AAD 類型身分識別提供者</span><span class="sxs-lookup"><span data-stu-id="07724-112">Get the AAD Type Identity Provider</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementIdentityProvider -Context $apimContext -Type Aad
```

<span data-ttu-id="07724-113">取得 Azure Active Directory 的身分識別提供者設定。</span><span class="sxs-lookup"><span data-stu-id="07724-113">Gets the Identity Provider Configuration of Azure Active Directory.</span></span>

## <span data-ttu-id="07724-114">參數</span><span class="sxs-lookup"><span data-stu-id="07724-114">PARAMETERS</span></span>

### <span data-ttu-id="07724-115">-內容</span><span class="sxs-lookup"><span data-stu-id="07724-115">-Context</span></span>
<span data-ttu-id="07724-116">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="07724-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="07724-117">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="07724-117">This parameter is required.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07724-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07724-118">-DefaultProfile</span></span>
<span data-ttu-id="07724-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="07724-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07724-120">-類型</span><span class="sxs-lookup"><span data-stu-id="07724-120">-Type</span></span>
<span data-ttu-id="07724-121">身分識別提供者的識別碼。</span><span class="sxs-lookup"><span data-stu-id="07724-121">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="07724-122">如果已指定，將會嘗試透過識別碼尋找身分識別提供者設定。</span><span class="sxs-lookup"><span data-stu-id="07724-122">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="07724-123">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="07724-123">This parameter is optional.</span></span>

```yaml
Type: PsApiManagementIdentityProviderType
Parameter Sets: IdentityProviderByType
Aliases: 
Accepted values: Facebook, Google, Microsoft, Twitter, Aad

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07724-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07724-124">CommonParameters</span></span>
<span data-ttu-id="07724-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="07724-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07724-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="07724-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07724-127">輸入</span><span class="sxs-lookup"><span data-stu-id="07724-127">INPUTS</span></span>

### <span data-ttu-id="07724-128">所有</span><span class="sxs-lookup"><span data-stu-id="07724-128">None</span></span>
<span data-ttu-id="07724-129">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="07724-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="07724-130">輸出</span><span class="sxs-lookup"><span data-stu-id="07724-130">OUTPUTS</span></span>

### <span data-ttu-id="07724-131">ServiceManagement. PsApiManagementIdentityProvider （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="07724-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>
<span data-ttu-id="07724-132">在 API 管理服務中設定之身分識別提供者的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="07724-132">The details of the Identity Provider configured in API Management service.</span></span>

### <span data-ttu-id="07724-133">IList<ApiManagement. ServiceManagement. PsApiManagementIdentityProvider]></span><span class="sxs-lookup"><span data-stu-id="07724-133">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider></span></span>
<span data-ttu-id="07724-134">在 API 管理服務中設定的身分識別提供者清單。</span><span class="sxs-lookup"><span data-stu-id="07724-134">The list of Identity Providers configured in API Management service.</span></span>

## <span data-ttu-id="07724-135">筆記</span><span class="sxs-lookup"><span data-stu-id="07724-135">NOTES</span></span>

## <span data-ttu-id="07724-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="07724-136">RELATED LINKS</span></span>

