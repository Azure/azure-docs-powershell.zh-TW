---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: D5B18FF4-3294-4561-A4CD-CF0FA5E4A59B
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: 2b66f8cbd82a1ea30554653aaaa61cabcbb589f6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613982"
---
# <span data-ttu-id="c0311-101">New-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="c0311-101">New-AzApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="c0311-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c0311-102">SYNOPSIS</span></span>
<span data-ttu-id="c0311-103">建立 OpenID 連接提供者。</span><span class="sxs-lookup"><span data-stu-id="c0311-103">Creates an OpenID Connect provider.</span></span>

## <span data-ttu-id="c0311-104">句法</span><span class="sxs-lookup"><span data-stu-id="c0311-104">SYNTAX</span></span>

```
New-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-OpenIdConnectProviderId <String>]
 -Name <String> -MetadataEndpointUri <String> -ClientId <String> [-ClientSecret <String>]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c0311-105">說明</span><span class="sxs-lookup"><span data-stu-id="c0311-105">DESCRIPTION</span></span>
<span data-ttu-id="c0311-106">**新的-AzApiManagementOpenIdConnectProvider** Cmdlet 會在 Azure API 管理中建立一個 OpenID connect 提供者。</span><span class="sxs-lookup"><span data-stu-id="c0311-106">The **New-AzApiManagementOpenIdConnectProvider** cmdlet creates an OpenID Connect provider in Azure API Management.</span></span>

## <span data-ttu-id="c0311-107">示例</span><span class="sxs-lookup"><span data-stu-id="c0311-107">EXAMPLES</span></span>

### <span data-ttu-id="c0311-108">範例1：建立提供者</span><span class="sxs-lookup"><span data-stu-id="c0311-108">Example 1: Create a provider</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvider01" -Name "Contoso OpenID Connect Provider" -MetadataEndpointUri "https://openid.provider/configuration" -ClientId "12432143" -Description "OpenID Connect provider description"
```

<span data-ttu-id="c0311-109">這個命令會建立一個名為 Contoso OpenID connect 提供者的 OpenID Connect **提供者**</span><span class="sxs-lookup"><span data-stu-id="c0311-109">This command creates an OpenID Connect **Provider** named Contoso OpenID Connect Provider</span></span>

## <span data-ttu-id="c0311-110">參數</span><span class="sxs-lookup"><span data-stu-id="c0311-110">PARAMETERS</span></span>

### <span data-ttu-id="c0311-111">-ClientId</span><span class="sxs-lookup"><span data-stu-id="c0311-111">-ClientId</span></span>
<span data-ttu-id="c0311-112">指定開發人員主控台的用戶端識別碼。</span><span class="sxs-lookup"><span data-stu-id="c0311-112">Specifies the client ID of the developer console.</span></span>

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

### <span data-ttu-id="c0311-113">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="c0311-113">-ClientSecret</span></span>
<span data-ttu-id="c0311-114">指定開發人員主控台的用戶端密碼。</span><span class="sxs-lookup"><span data-stu-id="c0311-114">Specifies the client secret of the developer console.</span></span>

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

### <span data-ttu-id="c0311-115">-內容</span><span class="sxs-lookup"><span data-stu-id="c0311-115">-Context</span></span>
<span data-ttu-id="c0311-116">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="c0311-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="c0311-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0311-117">-DefaultProfile</span></span>
<span data-ttu-id="c0311-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c0311-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c0311-119">-描述</span><span class="sxs-lookup"><span data-stu-id="c0311-119">-Description</span></span>
<span data-ttu-id="c0311-120">指定描述。</span><span class="sxs-lookup"><span data-stu-id="c0311-120">Specifies a description.</span></span>

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

### <span data-ttu-id="c0311-121">-MetadataEndpointUri</span><span class="sxs-lookup"><span data-stu-id="c0311-121">-MetadataEndpointUri</span></span>
<span data-ttu-id="c0311-122">指定提供者的中繼資料端點 URI。</span><span class="sxs-lookup"><span data-stu-id="c0311-122">Specifies a metadata endpoint URI of the provider.</span></span>

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

### <span data-ttu-id="c0311-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="c0311-123">-Name</span></span>
<span data-ttu-id="c0311-124">指定提供者的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="c0311-124">Specifies a friendly name for the provider.</span></span>

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

### <span data-ttu-id="c0311-125">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="c0311-125">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="c0311-126">指定提供者的識別碼。</span><span class="sxs-lookup"><span data-stu-id="c0311-126">Specifies an ID for the provider.</span></span>
<span data-ttu-id="c0311-127">如果您沒有指定識別碼，此 Cmdlet 會產生一個 ID。</span><span class="sxs-lookup"><span data-stu-id="c0311-127">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="c0311-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0311-128">CommonParameters</span></span>
<span data-ttu-id="c0311-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c0311-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0311-130">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c0311-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0311-131">輸入</span><span class="sxs-lookup"><span data-stu-id="c0311-131">INPUTS</span></span>

### <span data-ttu-id="c0311-132">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="c0311-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c0311-133">System.object</span><span class="sxs-lookup"><span data-stu-id="c0311-133">System.String</span></span>

## <span data-ttu-id="c0311-134">輸出</span><span class="sxs-lookup"><span data-stu-id="c0311-134">OUTPUTS</span></span>

### <span data-ttu-id="c0311-135">ServiceManagement. PsApiManagementOpenIdConnectProvider （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="c0311-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="c0311-136">筆記</span><span class="sxs-lookup"><span data-stu-id="c0311-136">NOTES</span></span>

## <span data-ttu-id="c0311-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="c0311-137">RELATED LINKS</span></span>

[<span data-ttu-id="c0311-138">AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="c0311-138">Get-AzApiManagementOpenIdConnectProvider</span></span>](./Get-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="c0311-139">移除-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="c0311-139">Remove-AzApiManagementOpenIdConnectProvider</span></span>](./Remove-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="c0311-140">Set-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="c0311-140">Set-AzApiManagementOpenIdConnectProvider</span></span>](./Set-AzApiManagementOpenIdConnectProvider.md)


