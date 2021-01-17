---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 15B6EAE2-56ED-4A01-B8EA-52B9FCDC1F66
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: 6968b4ea1b222d0f046611f10e65f8073a4ba86a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98447568"
---
# <span data-ttu-id="4e6c9-101">Get-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="4e6c9-101">Get-AzApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="4e6c9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4e6c9-102">SYNOPSIS</span></span>
<span data-ttu-id="4e6c9-103">取得 OpenID Connect 提供者。</span><span class="sxs-lookup"><span data-stu-id="4e6c9-103">Gets OpenID Connect providers.</span></span>

## <span data-ttu-id="4e6c9-104">句法</span><span class="sxs-lookup"><span data-stu-id="4e6c9-104">SYNTAX</span></span>

### <span data-ttu-id="4e6c9-105">GetAllOpenIdConnectProviders (預設) </span><span class="sxs-lookup"><span data-stu-id="4e6c9-105">GetAllOpenIdConnectProviders (Default)</span></span>
```
Get-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4e6c9-106">GetByOpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="4e6c9-106">GetByOpenIdConnectProviderId</span></span>
```
Get-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-OpenIdConnectProviderId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4e6c9-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="4e6c9-107">GetByName</span></span>
```
Get-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4e6c9-108">說明</span><span class="sxs-lookup"><span data-stu-id="4e6c9-108">DESCRIPTION</span></span>
<span data-ttu-id="4e6c9-109">**AzApiManagementOpenIdConnectProvider** Cmdlet 會在 Azure API 管理中取得 OpenID connect 提供者。</span><span class="sxs-lookup"><span data-stu-id="4e6c9-109">The **Get-AzApiManagementOpenIdConnectProvider** cmdlet gets OpenID Connect providers in Azure API Management.</span></span>
<span data-ttu-id="4e6c9-110">ClientSecret 不會包含在結果詳細資料中。</span><span class="sxs-lookup"><span data-stu-id="4e6c9-110">ClientSecret will not be included into result details.</span></span> <span data-ttu-id="4e6c9-111">若要取得用戶端密碼，請使用 **AzApiManagementOpenIdConnectProviderClientSecret**。</span><span class="sxs-lookup"><span data-stu-id="4e6c9-111">To get client secret, use **Get-AzApiManagementOpenIdConnectProviderClientSecret**.</span></span>

## <span data-ttu-id="4e6c9-112">示例</span><span class="sxs-lookup"><span data-stu-id="4e6c9-112">EXAMPLES</span></span>

### <span data-ttu-id="4e6c9-113">範例1：取得所有提供者</span><span class="sxs-lookup"><span data-stu-id="4e6c9-113">Example 1: Get all providers</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProvider -Context $apimContext
```

<span data-ttu-id="4e6c9-114">這個命令會取得指定內容的所有 OpenID 連接提供者。</span><span class="sxs-lookup"><span data-stu-id="4e6c9-114">This command gets all OpenID Connect providers for the specified context.</span></span>

### <span data-ttu-id="4e6c9-115">範例2：使用識別碼取得提供者</span><span class="sxs-lookup"><span data-stu-id="4e6c9-115">Example 2: Get a provider by using an ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvider01"
```

<span data-ttu-id="4e6c9-116">這個命令會取得 ID 為 OICProvider01 的提供者。</span><span class="sxs-lookup"><span data-stu-id="4e6c9-116">This command gets the provider that has the ID OICProvider01.</span></span>

### <span data-ttu-id="4e6c9-117">範例3：使用名稱取得提供者</span><span class="sxs-lookup"><span data-stu-id="4e6c9-117">Example 3: Get a provider by using a name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProvider -Context $apimContext -Name "Contoso OpenID Connect Provider"
```

<span data-ttu-id="4e6c9-118">這個命令會取得名為 Contoso OpenID Connect 提供者的提供者。</span><span class="sxs-lookup"><span data-stu-id="4e6c9-118">This command gets the provider named Contoso OpenID Connect Provider.</span></span>

## <span data-ttu-id="4e6c9-119">參數</span><span class="sxs-lookup"><span data-stu-id="4e6c9-119">PARAMETERS</span></span>

### <span data-ttu-id="4e6c9-120">-內容</span><span class="sxs-lookup"><span data-stu-id="4e6c9-120">-Context</span></span>
<span data-ttu-id="4e6c9-121">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="4e6c9-121">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="4e6c9-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e6c9-122">-DefaultProfile</span></span>
<span data-ttu-id="4e6c9-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4e6c9-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4e6c9-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="4e6c9-124">-Name</span></span>
<span data-ttu-id="4e6c9-125">指定提供者的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="4e6c9-125">Specifies a friendly name of a provider.</span></span>
<span data-ttu-id="4e6c9-126">如果您指定名稱，此 Cmdlet 會取得該提供者。</span><span class="sxs-lookup"><span data-stu-id="4e6c9-126">If you specify a name, this cmdlet gets that provider.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e6c9-127">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="4e6c9-127">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="4e6c9-128">指定此 Cmdlet 移除之提供者的識別碼。</span><span class="sxs-lookup"><span data-stu-id="4e6c9-128">Specifies an ID of the provider that this cmdlet removes.</span></span>
<span data-ttu-id="4e6c9-129">如果您指定 ID，此 Cmdlet 會取得該提供者。</span><span class="sxs-lookup"><span data-stu-id="4e6c9-129">If you specify an ID, this cmdlet gets that provider.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByOpenIdConnectProviderId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e6c9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e6c9-130">CommonParameters</span></span>
<span data-ttu-id="4e6c9-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4e6c9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e6c9-132">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="4e6c9-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e6c9-133">輸入</span><span class="sxs-lookup"><span data-stu-id="4e6c9-133">INPUTS</span></span>

### <span data-ttu-id="4e6c9-134">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="4e6c9-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="4e6c9-135">System.object</span><span class="sxs-lookup"><span data-stu-id="4e6c9-135">System.String</span></span>

## <span data-ttu-id="4e6c9-136">輸出</span><span class="sxs-lookup"><span data-stu-id="4e6c9-136">OUTPUTS</span></span>

### <span data-ttu-id="4e6c9-137">ServiceManagement. PsApiManagementOpenIdConnectProvider （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="4e6c9-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="4e6c9-138">筆記</span><span class="sxs-lookup"><span data-stu-id="4e6c9-138">NOTES</span></span>

## <span data-ttu-id="4e6c9-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="4e6c9-139">RELATED LINKS</span></span>

[<span data-ttu-id="4e6c9-140">新-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="4e6c9-140">New-AzApiManagementOpenIdConnectProvider</span></span>](./New-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="4e6c9-141">移除-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="4e6c9-141">Remove-AzApiManagementOpenIdConnectProvider</span></span>](./Remove-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="4e6c9-142">Set-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="4e6c9-142">Set-AzApiManagementOpenIdConnectProvider</span></span>](./Set-AzApiManagementOpenIdConnectProvider.md)


