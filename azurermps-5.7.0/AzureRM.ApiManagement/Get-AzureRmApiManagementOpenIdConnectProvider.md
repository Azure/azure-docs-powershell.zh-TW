---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 15B6EAE2-56ED-4A01-B8EA-52B9FCDC1F66
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: c26fb8991acc47ab655cb47c44194ca209423a70
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625039"
---
# <span data-ttu-id="f6325-101">Get-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="f6325-101">Get-AzureRmApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="f6325-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f6325-102">SYNOPSIS</span></span>
<span data-ttu-id="f6325-103">取得 OpenID Connect 提供者。</span><span class="sxs-lookup"><span data-stu-id="f6325-103">Gets OpenID Connect providers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f6325-104">句法</span><span class="sxs-lookup"><span data-stu-id="f6325-104">SYNTAX</span></span>

### <span data-ttu-id="f6325-105">GetAllOpenIdConnectProviders (預設) </span><span class="sxs-lookup"><span data-stu-id="f6325-105">GetAllOpenIdConnectProviders (Default)</span></span>
```
Get-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f6325-106">GetByOpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="f6325-106">GetByOpenIdConnectProviderId</span></span>
```
Get-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-OpenIdConnectProviderId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f6325-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="f6325-107">GetByName</span></span>
```
Get-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f6325-108">說明</span><span class="sxs-lookup"><span data-stu-id="f6325-108">DESCRIPTION</span></span>
<span data-ttu-id="f6325-109">**AzureRmApiManagementOpenIdConnectProvider** Cmdlet 會在 Azure API 管理中取得 OpenID connect 提供者。</span><span class="sxs-lookup"><span data-stu-id="f6325-109">The **Get-AzureRmApiManagementOpenIdConnectProvider** cmdlet gets OpenID Connect providers in Azure API Management.</span></span>

## <span data-ttu-id="f6325-110">示例</span><span class="sxs-lookup"><span data-stu-id="f6325-110">EXAMPLES</span></span>

### <span data-ttu-id="f6325-111">範例1：取得所有提供者</span><span class="sxs-lookup"><span data-stu-id="f6325-111">Example 1: Get all providers</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementOpenIdConnectProvider -Context $apimContext
```

<span data-ttu-id="f6325-112">這個命令會取得指定內容的所有 OpenID 連接提供者。</span><span class="sxs-lookup"><span data-stu-id="f6325-112">This command gets all OpenID Connect providers for the specified context.</span></span>

### <span data-ttu-id="f6325-113">範例2：使用識別碼取得提供者</span><span class="sxs-lookup"><span data-stu-id="f6325-113">Example 2: Get a provider by using an ID</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvicer01"
```

<span data-ttu-id="f6325-114">這個命令會取得 ID 為 OICProvicer01 的提供者。</span><span class="sxs-lookup"><span data-stu-id="f6325-114">This command gets the provider that has the ID OICProvicer01.</span></span>

### <span data-ttu-id="f6325-115">範例3：使用名稱取得提供者</span><span class="sxs-lookup"><span data-stu-id="f6325-115">Example 3: Get a provider by using a name</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementOpenIdConnectProvider -Context $apimContext -Name "Contoso OpenID Connect Provider"
```

<span data-ttu-id="f6325-116">這個命令會取得名為 Contoso OpenID Connect 提供者的提供者。</span><span class="sxs-lookup"><span data-stu-id="f6325-116">This command gets the provider named Contoso OpenID Connect Provider.</span></span>

## <span data-ttu-id="f6325-117">參數</span><span class="sxs-lookup"><span data-stu-id="f6325-117">PARAMETERS</span></span>

### <span data-ttu-id="f6325-118">-內容</span><span class="sxs-lookup"><span data-stu-id="f6325-118">-Context</span></span>
<span data-ttu-id="f6325-119">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="f6325-119">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="f6325-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6325-120">-DefaultProfile</span></span>
<span data-ttu-id="f6325-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f6325-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="f6325-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="f6325-122">-Name</span></span>
<span data-ttu-id="f6325-123">指定提供者的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="f6325-123">Specifies a friendly name of a provider.</span></span>
<span data-ttu-id="f6325-124">如果您指定名稱，此 Cmdlet 會取得該提供者。</span><span class="sxs-lookup"><span data-stu-id="f6325-124">If you specify a name, this cmdlet gets that provider.</span></span>

```yaml
Type: String
Parameter Sets: GetByName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6325-125">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="f6325-125">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="f6325-126">指定此 Cmdlet 移除之提供者的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f6325-126">Specifies an ID of the provider that this cmdlet removes.</span></span>
<span data-ttu-id="f6325-127">如果您指定 ID，此 Cmdlet 會取得該提供者。</span><span class="sxs-lookup"><span data-stu-id="f6325-127">If you specify an ID, this cmdlet gets that provider.</span></span>

```yaml
Type: String
Parameter Sets: GetByOpenIdConnectProviderId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6325-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6325-128">CommonParameters</span></span>
<span data-ttu-id="f6325-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f6325-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6325-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f6325-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6325-131">輸入</span><span class="sxs-lookup"><span data-stu-id="f6325-131">INPUTS</span></span>

### <span data-ttu-id="f6325-132">所有</span><span class="sxs-lookup"><span data-stu-id="f6325-132">None</span></span>
<span data-ttu-id="f6325-133">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="f6325-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f6325-134">輸出</span><span class="sxs-lookup"><span data-stu-id="f6325-134">OUTPUTS</span></span>

### <span data-ttu-id="f6325-135">ServiceManagement. PsApiManagementOpenIdConnectProvider （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="f6325-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>
<span data-ttu-id="f6325-136">在 API 管理服務中設定的 OpenId connect 提供者的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="f6325-136">The detail of the OpenId connect Provider configured in API Management service.</span></span>

### <span data-ttu-id="f6325-137">IList<ApiManagement. ServiceManagement. PsApiManagementOpenIdConnectProvider]></span><span class="sxs-lookup"><span data-stu-id="f6325-137">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider></span></span>
<span data-ttu-id="f6325-138">在 API 管理服務中設定的 OpenId 連接提供者清單。</span><span class="sxs-lookup"><span data-stu-id="f6325-138">The list of OpenId Connect Providers configured in API Management service.</span></span>

## <span data-ttu-id="f6325-139">筆記</span><span class="sxs-lookup"><span data-stu-id="f6325-139">NOTES</span></span>

## <span data-ttu-id="f6325-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="f6325-140">RELATED LINKS</span></span>

[<span data-ttu-id="f6325-141">新-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="f6325-141">New-AzureRmApiManagementOpenIdConnectProvider</span></span>](./New-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="f6325-142">移除-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="f6325-142">Remove-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Remove-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="f6325-143">Set-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="f6325-143">Set-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Set-AzureRmApiManagementOpenIdConnectProvider.md)


