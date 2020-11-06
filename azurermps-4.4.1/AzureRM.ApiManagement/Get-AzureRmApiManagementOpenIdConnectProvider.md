---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 15B6EAE2-56ED-4A01-B8EA-52B9FCDC1F66
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: d97090f6374890d9ae7ba24e53d6e1d60430f7b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445223"
---
# <span data-ttu-id="70a30-101">Get-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="70a30-101">Get-AzureRmApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="70a30-102">摘要</span><span class="sxs-lookup"><span data-stu-id="70a30-102">SYNOPSIS</span></span>
<span data-ttu-id="70a30-103">取得 OpenID Connect 提供者。</span><span class="sxs-lookup"><span data-stu-id="70a30-103">Gets OpenID Connect providers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="70a30-104">句法</span><span class="sxs-lookup"><span data-stu-id="70a30-104">SYNTAX</span></span>

### <span data-ttu-id="70a30-105">取得所有的 OpenID 連接提供者 (預設) </span><span class="sxs-lookup"><span data-stu-id="70a30-105">Get all OpenID Connect Providers (Default)</span></span>
```
Get-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="70a30-106">透過 OpenID 連接提供者識別碼來取得</span><span class="sxs-lookup"><span data-stu-id="70a30-106">Get by OpenID Connect Provider ID</span></span>
```
Get-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-OpenIdConnectProviderId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="70a30-107">依 OpenID 連接提供者易記名稱尋找</span><span class="sxs-lookup"><span data-stu-id="70a30-107">Find by OpenID Connect Provider friendly Name</span></span>
```
Get-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="70a30-108">說明</span><span class="sxs-lookup"><span data-stu-id="70a30-108">DESCRIPTION</span></span>
<span data-ttu-id="70a30-109">**AzureRmApiManagementOpenIdConnectProvider** Cmdlet 會在 Azure API 管理中取得 OpenID connect 提供者。</span><span class="sxs-lookup"><span data-stu-id="70a30-109">The **Get-AzureRmApiManagementOpenIdConnectProvider** cmdlet gets OpenID Connect providers in Azure API Management.</span></span>

## <span data-ttu-id="70a30-110">示例</span><span class="sxs-lookup"><span data-stu-id="70a30-110">EXAMPLES</span></span>

### <span data-ttu-id="70a30-111">範例1：取得所有提供者</span><span class="sxs-lookup"><span data-stu-id="70a30-111">Example 1: Get all providers</span></span>
```
PS C:\>Get-AzureRmApiManagementOpenIdConnectProvider -Context $ApimContext
```

<span data-ttu-id="70a30-112">這個命令會取得指定內容的所有 OpenID 連接提供者。</span><span class="sxs-lookup"><span data-stu-id="70a30-112">This command gets all OpenID Connect providers for the specified context.</span></span>

### <span data-ttu-id="70a30-113">範例2：使用識別碼取得提供者</span><span class="sxs-lookup"><span data-stu-id="70a30-113">Example 2: Get a provider by using an ID</span></span>
```
PS C:\>Get-AzureRmApiManagementOpenIdConnectProvider -Context $ApimContext -OpenIdConnectProviderId "OICProvicer01"
```

<span data-ttu-id="70a30-114">這個命令會取得 ID 為 OICProvicer01 的提供者。</span><span class="sxs-lookup"><span data-stu-id="70a30-114">This command gets the provider that has the ID OICProvicer01.</span></span>

### <span data-ttu-id="70a30-115">範例3：使用名稱取得提供者</span><span class="sxs-lookup"><span data-stu-id="70a30-115">Example 3: Get a provider by using a name</span></span>
```
PS C:\>Get-AzureRmApiManagementOpenIdConnectProvider -Context $ApimContext -Name "Contoso OpenID Connect Provider"
```

<span data-ttu-id="70a30-116">這個命令會取得名為 Contoso OpenID Connect 提供者的提供者。</span><span class="sxs-lookup"><span data-stu-id="70a30-116">This command gets the provider named Contoso OpenID Connect Provider.</span></span>

## <span data-ttu-id="70a30-117">參數</span><span class="sxs-lookup"><span data-stu-id="70a30-117">PARAMETERS</span></span>

### <span data-ttu-id="70a30-118">-內容</span><span class="sxs-lookup"><span data-stu-id="70a30-118">-Context</span></span>
<span data-ttu-id="70a30-119">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="70a30-119">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="70a30-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="70a30-120">-Name</span></span>
<span data-ttu-id="70a30-121">指定提供者的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="70a30-121">Specifies a friendly name of a provider.</span></span>
<span data-ttu-id="70a30-122">如果您指定名稱，此 Cmdlet 會取得該提供者。</span><span class="sxs-lookup"><span data-stu-id="70a30-122">If you specify a name, this cmdlet gets that provider.</span></span>

```yaml
Type: System.String
Parameter Sets: Find by OpenID Connect Provider friendly Name
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70a30-123">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="70a30-123">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="70a30-124">指定此 Cmdlet 移除之提供者的識別碼。</span><span class="sxs-lookup"><span data-stu-id="70a30-124">Specifies an ID of the provider that this cmdlet removes.</span></span>
<span data-ttu-id="70a30-125">如果您指定 ID，此 Cmdlet 會取得該提供者。</span><span class="sxs-lookup"><span data-stu-id="70a30-125">If you specify an ID, this cmdlet gets that provider.</span></span>

```yaml
Type: System.String
Parameter Sets: Get by OpenID Connect Provider ID
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70a30-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70a30-126">-DefaultProfile</span></span>
<span data-ttu-id="70a30-127">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="70a30-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="70a30-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70a30-128">CommonParameters</span></span>
<span data-ttu-id="70a30-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="70a30-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70a30-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="70a30-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70a30-131">輸入</span><span class="sxs-lookup"><span data-stu-id="70a30-131">INPUTS</span></span>

## <span data-ttu-id="70a30-132">輸出</span><span class="sxs-lookup"><span data-stu-id="70a30-132">OUTPUTS</span></span>

### <span data-ttu-id="70a30-133">IList<ApiManagement. ServiceManagement. PsApiManagementOpenIdConnectProvider]></span><span class="sxs-lookup"><span data-stu-id="70a30-133">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider></span></span>

## <span data-ttu-id="70a30-134">筆記</span><span class="sxs-lookup"><span data-stu-id="70a30-134">NOTES</span></span>

## <span data-ttu-id="70a30-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="70a30-135">RELATED LINKS</span></span>

[<span data-ttu-id="70a30-136">新-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="70a30-136">New-AzureRmApiManagementOpenIdConnectProvider</span></span>](./New-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="70a30-137">移除-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="70a30-137">Remove-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Remove-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="70a30-138">Set-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="70a30-138">Set-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Set-AzureRmApiManagementOpenIdConnectProvider.md)


