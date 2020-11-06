---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 15B6EAE2-56ED-4A01-B8EA-52B9FCDC1F66
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: cdc1341296349897b1ccc2e27785c3cd48360ddb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93614044"
---
# <span data-ttu-id="0d9de-101">Get-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="0d9de-101">Get-AzApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="0d9de-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0d9de-102">SYNOPSIS</span></span>
<span data-ttu-id="0d9de-103">取得 OpenID Connect 提供者。</span><span class="sxs-lookup"><span data-stu-id="0d9de-103">Gets OpenID Connect providers.</span></span>

## <span data-ttu-id="0d9de-104">句法</span><span class="sxs-lookup"><span data-stu-id="0d9de-104">SYNTAX</span></span>

### <span data-ttu-id="0d9de-105">GetAllOpenIdConnectProviders (預設) </span><span class="sxs-lookup"><span data-stu-id="0d9de-105">GetAllOpenIdConnectProviders (Default)</span></span>
```
Get-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0d9de-106">GetByOpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="0d9de-106">GetByOpenIdConnectProviderId</span></span>
```
Get-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-OpenIdConnectProviderId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0d9de-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="0d9de-107">GetByName</span></span>
```
Get-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d9de-108">說明</span><span class="sxs-lookup"><span data-stu-id="0d9de-108">DESCRIPTION</span></span>
<span data-ttu-id="0d9de-109">**AzApiManagementOpenIdConnectProvider** Cmdlet 會在 Azure API 管理中取得 OpenID connect 提供者。</span><span class="sxs-lookup"><span data-stu-id="0d9de-109">The **Get-AzApiManagementOpenIdConnectProvider** cmdlet gets OpenID Connect providers in Azure API Management.</span></span>

## <span data-ttu-id="0d9de-110">示例</span><span class="sxs-lookup"><span data-stu-id="0d9de-110">EXAMPLES</span></span>

### <span data-ttu-id="0d9de-111">範例1：取得所有提供者</span><span class="sxs-lookup"><span data-stu-id="0d9de-111">Example 1: Get all providers</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProvider -Context $apimContext
```

<span data-ttu-id="0d9de-112">這個命令會取得指定內容的所有 OpenID 連接提供者。</span><span class="sxs-lookup"><span data-stu-id="0d9de-112">This command gets all OpenID Connect providers for the specified context.</span></span>

### <span data-ttu-id="0d9de-113">範例2：使用識別碼取得提供者</span><span class="sxs-lookup"><span data-stu-id="0d9de-113">Example 2: Get a provider by using an ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvider01"
```

<span data-ttu-id="0d9de-114">這個命令會取得 ID 為 OICProvider01 的提供者。</span><span class="sxs-lookup"><span data-stu-id="0d9de-114">This command gets the provider that has the ID OICProvider01.</span></span>

### <span data-ttu-id="0d9de-115">範例3：使用名稱取得提供者</span><span class="sxs-lookup"><span data-stu-id="0d9de-115">Example 3: Get a provider by using a name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProvider -Context $apimContext -Name "Contoso OpenID Connect Provider"
```

<span data-ttu-id="0d9de-116">這個命令會取得名為 Contoso OpenID Connect 提供者的提供者。</span><span class="sxs-lookup"><span data-stu-id="0d9de-116">This command gets the provider named Contoso OpenID Connect Provider.</span></span>

## <span data-ttu-id="0d9de-117">參數</span><span class="sxs-lookup"><span data-stu-id="0d9de-117">PARAMETERS</span></span>

### <span data-ttu-id="0d9de-118">-內容</span><span class="sxs-lookup"><span data-stu-id="0d9de-118">-Context</span></span>
<span data-ttu-id="0d9de-119">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="0d9de-119">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="0d9de-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d9de-120">-DefaultProfile</span></span>
<span data-ttu-id="0d9de-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0d9de-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d9de-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="0d9de-122">-Name</span></span>
<span data-ttu-id="0d9de-123">指定提供者的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="0d9de-123">Specifies a friendly name of a provider.</span></span>
<span data-ttu-id="0d9de-124">如果您指定名稱，此 Cmdlet 會取得該提供者。</span><span class="sxs-lookup"><span data-stu-id="0d9de-124">If you specify a name, this cmdlet gets that provider.</span></span>

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

### <span data-ttu-id="0d9de-125">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="0d9de-125">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="0d9de-126">指定此 Cmdlet 移除之提供者的識別碼。</span><span class="sxs-lookup"><span data-stu-id="0d9de-126">Specifies an ID of the provider that this cmdlet removes.</span></span>
<span data-ttu-id="0d9de-127">如果您指定 ID，此 Cmdlet 會取得該提供者。</span><span class="sxs-lookup"><span data-stu-id="0d9de-127">If you specify an ID, this cmdlet gets that provider.</span></span>

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

### <span data-ttu-id="0d9de-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d9de-128">CommonParameters</span></span>
<span data-ttu-id="0d9de-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0d9de-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d9de-130">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="0d9de-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d9de-131">輸入</span><span class="sxs-lookup"><span data-stu-id="0d9de-131">INPUTS</span></span>

### <span data-ttu-id="0d9de-132">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="0d9de-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="0d9de-133">System.object</span><span class="sxs-lookup"><span data-stu-id="0d9de-133">System.String</span></span>

## <span data-ttu-id="0d9de-134">輸出</span><span class="sxs-lookup"><span data-stu-id="0d9de-134">OUTPUTS</span></span>

### <span data-ttu-id="0d9de-135">ServiceManagement. PsApiManagementOpenIdConnectProvider （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="0d9de-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="0d9de-136">筆記</span><span class="sxs-lookup"><span data-stu-id="0d9de-136">NOTES</span></span>

## <span data-ttu-id="0d9de-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="0d9de-137">RELATED LINKS</span></span>

[<span data-ttu-id="0d9de-138">新-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="0d9de-138">New-AzApiManagementOpenIdConnectProvider</span></span>](./New-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="0d9de-139">移除-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="0d9de-139">Remove-AzApiManagementOpenIdConnectProvider</span></span>](./Remove-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="0d9de-140">Set-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="0d9de-140">Set-AzApiManagementOpenIdConnectProvider</span></span>](./Set-AzApiManagementOpenIdConnectProvider.md)


