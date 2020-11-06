---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: D5B18FF4-3294-4561-A4CD-CF0FA5E4A59B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: f008d21e1d1d3f2aba7c87255fa7c95074bca532
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450101"
---
# <span data-ttu-id="d038b-101">New-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="d038b-101">New-AzureRmApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="d038b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d038b-102">SYNOPSIS</span></span>
<span data-ttu-id="d038b-103">建立 OpenID 連接提供者。</span><span class="sxs-lookup"><span data-stu-id="d038b-103">Creates an OpenID Connect provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d038b-104">句法</span><span class="sxs-lookup"><span data-stu-id="d038b-104">SYNTAX</span></span>

```
New-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-OpenIdConnectProviderId <String>] -Name <String> -MetadataEndpointUri <String> -ClientId <String>
 [-ClientSecret <String>] [-Description <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d038b-105">說明</span><span class="sxs-lookup"><span data-stu-id="d038b-105">DESCRIPTION</span></span>
<span data-ttu-id="d038b-106">**新的-AzureRmApiManagementOpenIdConnectProvider** Cmdlet 會在 Azure API 管理中建立一個 OpenID connect 提供者。</span><span class="sxs-lookup"><span data-stu-id="d038b-106">The **New-AzureRmApiManagementOpenIdConnectProvider** cmdlet creates an OpenID Connect provider in Azure API Management.</span></span>

## <span data-ttu-id="d038b-107">示例</span><span class="sxs-lookup"><span data-stu-id="d038b-107">EXAMPLES</span></span>

### <span data-ttu-id="d038b-108">範例1：建立提供者</span><span class="sxs-lookup"><span data-stu-id="d038b-108">Example 1: Create a provider</span></span>
```
PS C:\>New-AzureRmApiManagementOpenIdConnectProvider -Context $ApimContext -OpenIdConnectProviderId "OICProvicer01" -Name "Contoso OpenID Connect Provider" -MetadataEndpointUri "https://openid.provider/configuration" -ClientId "12432143" -Description "OpenID Connect provider description"
```

<span data-ttu-id="d038b-109">這個命令會建立一個名為 Contoso OpenID connect 提供者的 OpenID Connect **提供者**</span><span class="sxs-lookup"><span data-stu-id="d038b-109">This command creates an OpenID Connect **Provider** named Contoso OpenID Connect Provider</span></span>

## <span data-ttu-id="d038b-110">參數</span><span class="sxs-lookup"><span data-stu-id="d038b-110">PARAMETERS</span></span>

### <span data-ttu-id="d038b-111">-ClientId</span><span class="sxs-lookup"><span data-stu-id="d038b-111">-ClientId</span></span>
<span data-ttu-id="d038b-112">指定開發人員主控台的用戶端識別碼。</span><span class="sxs-lookup"><span data-stu-id="d038b-112">Specifies the client ID of the developer console.</span></span>

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

### <span data-ttu-id="d038b-113">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="d038b-113">-ClientSecret</span></span>
<span data-ttu-id="d038b-114">指定開發人員主控台的用戶端密碼。</span><span class="sxs-lookup"><span data-stu-id="d038b-114">Specifies the client secret of the developer console.</span></span>

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

### <span data-ttu-id="d038b-115">-內容</span><span class="sxs-lookup"><span data-stu-id="d038b-115">-Context</span></span>
<span data-ttu-id="d038b-116">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="d038b-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="d038b-117">-描述</span><span class="sxs-lookup"><span data-stu-id="d038b-117">-Description</span></span>
<span data-ttu-id="d038b-118">指定描述。</span><span class="sxs-lookup"><span data-stu-id="d038b-118">Specifies a description.</span></span>

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

### <span data-ttu-id="d038b-119">-MetadataEndpointUri</span><span class="sxs-lookup"><span data-stu-id="d038b-119">-MetadataEndpointUri</span></span>
<span data-ttu-id="d038b-120">指定提供者的中繼資料端點 URI。</span><span class="sxs-lookup"><span data-stu-id="d038b-120">Specifies a metadata endpoint URI of the provider.</span></span>

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

### <span data-ttu-id="d038b-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="d038b-121">-Name</span></span>
<span data-ttu-id="d038b-122">指定提供者的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="d038b-122">Specifies a friendly name for the provider.</span></span>

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

### <span data-ttu-id="d038b-123">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="d038b-123">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="d038b-124">指定提供者的識別碼。</span><span class="sxs-lookup"><span data-stu-id="d038b-124">Specifies an ID for the provider.</span></span>
<span data-ttu-id="d038b-125">如果您沒有指定識別碼，此 Cmdlet 會產生一個 ID。</span><span class="sxs-lookup"><span data-stu-id="d038b-125">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="d038b-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d038b-126">-DefaultProfile</span></span>
<span data-ttu-id="d038b-127">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d038b-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d038b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d038b-128">CommonParameters</span></span>
<span data-ttu-id="d038b-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d038b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d038b-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d038b-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d038b-131">輸入</span><span class="sxs-lookup"><span data-stu-id="d038b-131">INPUTS</span></span>

## <span data-ttu-id="d038b-132">輸出</span><span class="sxs-lookup"><span data-stu-id="d038b-132">OUTPUTS</span></span>

### <span data-ttu-id="d038b-133">ServiceManagement. PsApiManagementOpenIdConnectProvider （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="d038b-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="d038b-134">筆記</span><span class="sxs-lookup"><span data-stu-id="d038b-134">NOTES</span></span>

## <span data-ttu-id="d038b-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="d038b-135">RELATED LINKS</span></span>

[<span data-ttu-id="d038b-136">AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="d038b-136">Get-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Get-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="d038b-137">移除-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="d038b-137">Remove-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Remove-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="d038b-138">Set-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="d038b-138">Set-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Set-AzureRmApiManagementOpenIdConnectProvider.md)


