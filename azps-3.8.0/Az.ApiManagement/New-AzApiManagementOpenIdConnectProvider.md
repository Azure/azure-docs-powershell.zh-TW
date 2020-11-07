---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: D5B18FF4-3294-4561-A4CD-CF0FA5E4A59B
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: 37144ab119eba4f19c3b34b2b32dfd28ff305677
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958165"
---
# <span data-ttu-id="fc11b-101">New-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="fc11b-101">New-AzApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="fc11b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fc11b-102">SYNOPSIS</span></span>
<span data-ttu-id="fc11b-103">建立 OpenID 連接提供者。</span><span class="sxs-lookup"><span data-stu-id="fc11b-103">Creates an OpenID Connect provider.</span></span>

## <span data-ttu-id="fc11b-104">句法</span><span class="sxs-lookup"><span data-stu-id="fc11b-104">SYNTAX</span></span>

```
New-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-OpenIdConnectProviderId <String>]
 -Name <String> -MetadataEndpointUri <String> -ClientId <String> [-ClientSecret <String>]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc11b-105">說明</span><span class="sxs-lookup"><span data-stu-id="fc11b-105">DESCRIPTION</span></span>
<span data-ttu-id="fc11b-106">**新的-AzApiManagementOpenIdConnectProvider** Cmdlet 會在 Azure API 管理中建立一個 OpenID connect 提供者。</span><span class="sxs-lookup"><span data-stu-id="fc11b-106">The **New-AzApiManagementOpenIdConnectProvider** cmdlet creates an OpenID Connect provider in Azure API Management.</span></span>

## <span data-ttu-id="fc11b-107">示例</span><span class="sxs-lookup"><span data-stu-id="fc11b-107">EXAMPLES</span></span>

### <span data-ttu-id="fc11b-108">範例1：建立提供者</span><span class="sxs-lookup"><span data-stu-id="fc11b-108">Example 1: Create a provider</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvider01" -Name "Contoso OpenID Connect Provider" -MetadataEndpointUri "https://openid.provider/configuration" -ClientId "12432143" -Description "OpenID Connect provider description"
```

<span data-ttu-id="fc11b-109">這個命令會建立一個名為 Contoso OpenID connect 提供者的 OpenID Connect **提供者**</span><span class="sxs-lookup"><span data-stu-id="fc11b-109">This command creates an OpenID Connect **Provider** named Contoso OpenID Connect Provider</span></span>

## <span data-ttu-id="fc11b-110">參數</span><span class="sxs-lookup"><span data-stu-id="fc11b-110">PARAMETERS</span></span>

### <span data-ttu-id="fc11b-111">-ClientId</span><span class="sxs-lookup"><span data-stu-id="fc11b-111">-ClientId</span></span>
<span data-ttu-id="fc11b-112">指定開發人員主控台的用戶端識別碼。</span><span class="sxs-lookup"><span data-stu-id="fc11b-112">Specifies the client ID of the developer console.</span></span>

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

### <span data-ttu-id="fc11b-113">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="fc11b-113">-ClientSecret</span></span>
<span data-ttu-id="fc11b-114">指定開發人員主控台的用戶端密碼。</span><span class="sxs-lookup"><span data-stu-id="fc11b-114">Specifies the client secret of the developer console.</span></span>

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

### <span data-ttu-id="fc11b-115">-內容</span><span class="sxs-lookup"><span data-stu-id="fc11b-115">-Context</span></span>
<span data-ttu-id="fc11b-116">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="fc11b-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="fc11b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc11b-117">-DefaultProfile</span></span>
<span data-ttu-id="fc11b-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fc11b-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fc11b-119">-描述</span><span class="sxs-lookup"><span data-stu-id="fc11b-119">-Description</span></span>
<span data-ttu-id="fc11b-120">指定描述。</span><span class="sxs-lookup"><span data-stu-id="fc11b-120">Specifies a description.</span></span>

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

### <span data-ttu-id="fc11b-121">-MetadataEndpointUri</span><span class="sxs-lookup"><span data-stu-id="fc11b-121">-MetadataEndpointUri</span></span>
<span data-ttu-id="fc11b-122">指定提供者的中繼資料端點 URI。</span><span class="sxs-lookup"><span data-stu-id="fc11b-122">Specifies a metadata endpoint URI of the provider.</span></span>

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

### <span data-ttu-id="fc11b-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="fc11b-123">-Name</span></span>
<span data-ttu-id="fc11b-124">指定提供者的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="fc11b-124">Specifies a friendly name for the provider.</span></span>

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

### <span data-ttu-id="fc11b-125">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="fc11b-125">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="fc11b-126">指定提供者的識別碼。</span><span class="sxs-lookup"><span data-stu-id="fc11b-126">Specifies an ID for the provider.</span></span>
<span data-ttu-id="fc11b-127">如果您沒有指定識別碼，此 Cmdlet 會產生一個 ID。</span><span class="sxs-lookup"><span data-stu-id="fc11b-127">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="fc11b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc11b-128">CommonParameters</span></span>
<span data-ttu-id="fc11b-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fc11b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc11b-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="fc11b-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc11b-131">輸入</span><span class="sxs-lookup"><span data-stu-id="fc11b-131">INPUTS</span></span>

### <span data-ttu-id="fc11b-132">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="fc11b-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="fc11b-133">System.object</span><span class="sxs-lookup"><span data-stu-id="fc11b-133">System.String</span></span>

## <span data-ttu-id="fc11b-134">輸出</span><span class="sxs-lookup"><span data-stu-id="fc11b-134">OUTPUTS</span></span>

### <span data-ttu-id="fc11b-135">ServiceManagement. PsApiManagementOpenIdConnectProvider （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="fc11b-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="fc11b-136">筆記</span><span class="sxs-lookup"><span data-stu-id="fc11b-136">NOTES</span></span>

## <span data-ttu-id="fc11b-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="fc11b-137">RELATED LINKS</span></span>

[<span data-ttu-id="fc11b-138">AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="fc11b-138">Get-AzApiManagementOpenIdConnectProvider</span></span>](./Get-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="fc11b-139">移除-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="fc11b-139">Remove-AzApiManagementOpenIdConnectProvider</span></span>](./Remove-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="fc11b-140">Set-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="fc11b-140">Set-AzApiManagementOpenIdConnectProvider</span></span>](./Set-AzApiManagementOpenIdConnectProvider.md)


