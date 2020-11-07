---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: D5B18FF4-3294-4561-A4CD-CF0FA5E4A59B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: c338cd8b2ea3ce2a464a7975ecac959bc1e52140
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624638"
---
# <span data-ttu-id="2d797-101">New-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="2d797-101">New-AzureRmApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="2d797-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2d797-102">SYNOPSIS</span></span>
<span data-ttu-id="2d797-103">建立 OpenID 連接提供者。</span><span class="sxs-lookup"><span data-stu-id="2d797-103">Creates an OpenID Connect provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2d797-104">句法</span><span class="sxs-lookup"><span data-stu-id="2d797-104">SYNTAX</span></span>

```
New-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-OpenIdConnectProviderId <String>] -Name <String> -MetadataEndpointUri <String> -ClientId <String>
 [-ClientSecret <String>] [-Description <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2d797-105">說明</span><span class="sxs-lookup"><span data-stu-id="2d797-105">DESCRIPTION</span></span>
<span data-ttu-id="2d797-106">**新的-AzureRmApiManagementOpenIdConnectProvider** Cmdlet 會在 Azure API 管理中建立一個 OpenID connect 提供者。</span><span class="sxs-lookup"><span data-stu-id="2d797-106">The **New-AzureRmApiManagementOpenIdConnectProvider** cmdlet creates an OpenID Connect provider in Azure API Management.</span></span>

## <span data-ttu-id="2d797-107">示例</span><span class="sxs-lookup"><span data-stu-id="2d797-107">EXAMPLES</span></span>

### <span data-ttu-id="2d797-108">範例1：建立提供者</span><span class="sxs-lookup"><span data-stu-id="2d797-108">Example 1: Create a provider</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvicer01" -Name "Contoso OpenID Connect Provider" -MetadataEndpointUri "https://openid.provider/configuration" -ClientId "12432143" -Description "OpenID Connect provider description"
```

<span data-ttu-id="2d797-109">這個命令會建立一個名為 Contoso OpenID connect 提供者的 OpenID Connect **提供者**</span><span class="sxs-lookup"><span data-stu-id="2d797-109">This command creates an OpenID Connect **Provider** named Contoso OpenID Connect Provider</span></span>

## <span data-ttu-id="2d797-110">參數</span><span class="sxs-lookup"><span data-stu-id="2d797-110">PARAMETERS</span></span>

### <span data-ttu-id="2d797-111">-ClientId</span><span class="sxs-lookup"><span data-stu-id="2d797-111">-ClientId</span></span>
<span data-ttu-id="2d797-112">指定開發人員主控台的用戶端識別碼。</span><span class="sxs-lookup"><span data-stu-id="2d797-112">Specifies the client ID of the developer console.</span></span>

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

### <span data-ttu-id="2d797-113">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="2d797-113">-ClientSecret</span></span>
<span data-ttu-id="2d797-114">指定開發人員主控台的用戶端密碼。</span><span class="sxs-lookup"><span data-stu-id="2d797-114">Specifies the client secret of the developer console.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d797-115">-內容</span><span class="sxs-lookup"><span data-stu-id="2d797-115">-Context</span></span>
<span data-ttu-id="2d797-116">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="2d797-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="2d797-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d797-117">-DefaultProfile</span></span>
<span data-ttu-id="2d797-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2d797-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2d797-119">-描述</span><span class="sxs-lookup"><span data-stu-id="2d797-119">-Description</span></span>
<span data-ttu-id="2d797-120">指定描述。</span><span class="sxs-lookup"><span data-stu-id="2d797-120">Specifies a description.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d797-121">-MetadataEndpointUri</span><span class="sxs-lookup"><span data-stu-id="2d797-121">-MetadataEndpointUri</span></span>
<span data-ttu-id="2d797-122">指定提供者的中繼資料端點 URI。</span><span class="sxs-lookup"><span data-stu-id="2d797-122">Specifies a metadata endpoint URI of the provider.</span></span>

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

### <span data-ttu-id="2d797-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="2d797-123">-Name</span></span>
<span data-ttu-id="2d797-124">指定提供者的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="2d797-124">Specifies a friendly name for the provider.</span></span>

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

### <span data-ttu-id="2d797-125">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="2d797-125">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="2d797-126">指定提供者的識別碼。</span><span class="sxs-lookup"><span data-stu-id="2d797-126">Specifies an ID for the provider.</span></span>
<span data-ttu-id="2d797-127">如果您沒有指定識別碼，此 Cmdlet 會產生一個 ID。</span><span class="sxs-lookup"><span data-stu-id="2d797-127">If you do not specify an ID, this cmdlet generates one.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d797-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d797-128">CommonParameters</span></span>
<span data-ttu-id="2d797-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2d797-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d797-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2d797-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d797-131">輸入</span><span class="sxs-lookup"><span data-stu-id="2d797-131">INPUTS</span></span>

### <span data-ttu-id="2d797-132">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="2d797-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2d797-133">System.object</span><span class="sxs-lookup"><span data-stu-id="2d797-133">System.String</span></span>

## <span data-ttu-id="2d797-134">輸出</span><span class="sxs-lookup"><span data-stu-id="2d797-134">OUTPUTS</span></span>

### <span data-ttu-id="2d797-135">ServiceManagement. PsApiManagementOpenIdConnectProvider （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="2d797-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="2d797-136">筆記</span><span class="sxs-lookup"><span data-stu-id="2d797-136">NOTES</span></span>

## <span data-ttu-id="2d797-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="2d797-137">RELATED LINKS</span></span>

[<span data-ttu-id="2d797-138">AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="2d797-138">Get-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Get-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="2d797-139">移除-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="2d797-139">Remove-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Remove-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="2d797-140">Set-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="2d797-140">Set-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Set-AzureRmApiManagementOpenIdConnectProvider.md)


