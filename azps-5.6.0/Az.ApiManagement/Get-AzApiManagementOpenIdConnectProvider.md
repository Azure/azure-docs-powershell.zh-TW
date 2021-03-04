---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 15B6EAE2-56ED-4A01-B8EA-52B9FCDC1F66
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: 1a46cccc38e1b562786e9eda88f3336430559fc0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917517"
---
# <span data-ttu-id="120d1-101">Get-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="120d1-101">Get-AzApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="120d1-102">簡介</span><span class="sxs-lookup"><span data-stu-id="120d1-102">SYNOPSIS</span></span>
<span data-ttu-id="120d1-103">獲得 OpenID Connect 提供者。</span><span class="sxs-lookup"><span data-stu-id="120d1-103">Gets OpenID Connect providers.</span></span>

## <span data-ttu-id="120d1-104">語法</span><span class="sxs-lookup"><span data-stu-id="120d1-104">SYNTAX</span></span>

### <span data-ttu-id="120d1-105">GetAllOpenIdConnectProviders (預設) </span><span class="sxs-lookup"><span data-stu-id="120d1-105">GetAllOpenIdConnectProviders (Default)</span></span>
```
Get-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="120d1-106">GetByOpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="120d1-106">GetByOpenIdConnectProviderId</span></span>
```
Get-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-OpenIdConnectProviderId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="120d1-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="120d1-107">GetByName</span></span>
```
Get-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="120d1-108">描述</span><span class="sxs-lookup"><span data-stu-id="120d1-108">DESCRIPTION</span></span>
<span data-ttu-id="120d1-109">**Get-AzApiManagementOpenIdConnectProvider Cmdlet** 會取得 Azure API 管理中的 OpenID Connect 提供者。</span><span class="sxs-lookup"><span data-stu-id="120d1-109">The **Get-AzApiManagementOpenIdConnectProvider** cmdlet gets OpenID Connect providers in Azure API Management.</span></span>
<span data-ttu-id="120d1-110">ClientSecret 不會包含在結果詳細資料中。</span><span class="sxs-lookup"><span data-stu-id="120d1-110">ClientSecret will not be included into result details.</span></span> <span data-ttu-id="120d1-111">若要取得用戶端機密，請使用 **Get-AzApiManagementOpenIdConnectProviderClientSecret。**</span><span class="sxs-lookup"><span data-stu-id="120d1-111">To get client secret, use **Get-AzApiManagementOpenIdConnectProviderClientSecret**.</span></span>

## <span data-ttu-id="120d1-112">例子</span><span class="sxs-lookup"><span data-stu-id="120d1-112">EXAMPLES</span></span>

### <span data-ttu-id="120d1-113">範例 1：取得所有提供者</span><span class="sxs-lookup"><span data-stu-id="120d1-113">Example 1: Get all providers</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProvider -Context $apimContext
```

<span data-ttu-id="120d1-114">此命令會針對指定的上下文獲得所有 OpenID Connect 提供者。</span><span class="sxs-lookup"><span data-stu-id="120d1-114">This command gets all OpenID Connect providers for the specified context.</span></span>

### <span data-ttu-id="120d1-115">範例 2：使用識別碼取得提供者</span><span class="sxs-lookup"><span data-stu-id="120d1-115">Example 2: Get a provider by using an ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvider01"
```

<span data-ttu-id="120d1-116">此命令會獲得具有識別碼為 ISPPROvider01 的提供者。</span><span class="sxs-lookup"><span data-stu-id="120d1-116">This command gets the provider that has the ID OICProvider01.</span></span>

### <span data-ttu-id="120d1-117">範例 3：使用名稱取得提供者</span><span class="sxs-lookup"><span data-stu-id="120d1-117">Example 3: Get a provider by using a name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProvider -Context $apimContext -Name "Contoso OpenID Connect Provider"
```

<span data-ttu-id="120d1-118">此命令會獲得名為 Contoso OpenID Connect Provider 的提供者。</span><span class="sxs-lookup"><span data-stu-id="120d1-118">This command gets the provider named Contoso OpenID Connect Provider.</span></span>

## <span data-ttu-id="120d1-119">參數</span><span class="sxs-lookup"><span data-stu-id="120d1-119">PARAMETERS</span></span>

### <span data-ttu-id="120d1-120">-內容</span><span class="sxs-lookup"><span data-stu-id="120d1-120">-Context</span></span>
<span data-ttu-id="120d1-121">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="120d1-121">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="120d1-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="120d1-122">-DefaultProfile</span></span>
<span data-ttu-id="120d1-123">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="120d1-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="120d1-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="120d1-124">-Name</span></span>
<span data-ttu-id="120d1-125">指定提供者的好用名稱。</span><span class="sxs-lookup"><span data-stu-id="120d1-125">Specifies a friendly name of a provider.</span></span>
<span data-ttu-id="120d1-126">如果您指定名稱，此 Cmdlet 會獲得該提供者。</span><span class="sxs-lookup"><span data-stu-id="120d1-126">If you specify a name, this cmdlet gets that provider.</span></span>

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

### <span data-ttu-id="120d1-127">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="120d1-127">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="120d1-128">指定此 Cmdlet 移除的提供者識別碼。</span><span class="sxs-lookup"><span data-stu-id="120d1-128">Specifies an ID of the provider that this cmdlet removes.</span></span>
<span data-ttu-id="120d1-129">如果您指定識別碼，此 Cmdlet 會獲得該提供者。</span><span class="sxs-lookup"><span data-stu-id="120d1-129">If you specify an ID, this cmdlet gets that provider.</span></span>

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

### <span data-ttu-id="120d1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="120d1-130">CommonParameters</span></span>
<span data-ttu-id="120d1-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="120d1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="120d1-132">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="120d1-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="120d1-133">輸入</span><span class="sxs-lookup"><span data-stu-id="120d1-133">INPUTS</span></span>

### <span data-ttu-id="120d1-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCoNtext</span><span class="sxs-lookup"><span data-stu-id="120d1-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="120d1-135">System.String</span><span class="sxs-lookup"><span data-stu-id="120d1-135">System.String</span></span>

## <span data-ttu-id="120d1-136">輸出</span><span class="sxs-lookup"><span data-stu-id="120d1-136">OUTPUTS</span></span>

### <span data-ttu-id="120d1-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="120d1-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="120d1-138">筆記</span><span class="sxs-lookup"><span data-stu-id="120d1-138">NOTES</span></span>

## <span data-ttu-id="120d1-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="120d1-139">RELATED LINKS</span></span>

[<span data-ttu-id="120d1-140">New-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="120d1-140">New-AzApiManagementOpenIdConnectProvider</span></span>](./New-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="120d1-141">Remove-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="120d1-141">Remove-AzApiManagementOpenIdConnectProvider</span></span>](./Remove-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="120d1-142">Set-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="120d1-142">Set-AzApiManagementOpenIdConnectProvider</span></span>](./Set-AzApiManagementOpenIdConnectProvider.md)


