---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPublicIpPrefix.md
ms.openlocfilehash: 6083c87ddf0bd7b2306fdacc6d109ccebc144faa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902449"
---
# <span data-ttu-id="11be0-101">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="11be0-101">Get-AzPublicIpPrefix</span></span>

## <span data-ttu-id="11be0-102">簡介</span><span class="sxs-lookup"><span data-stu-id="11be0-102">SYNOPSIS</span></span>
<span data-ttu-id="11be0-103">獲得公用 IP 首碼</span><span class="sxs-lookup"><span data-stu-id="11be0-103">Gets a public IP prefix</span></span>

## <span data-ttu-id="11be0-104">語法</span><span class="sxs-lookup"><span data-stu-id="11be0-104">SYNTAX</span></span>

### <span data-ttu-id="11be0-105">ListParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="11be0-105">ListParameterSet (Default)</span></span>
```
Get-AzPublicIpPrefix [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="11be0-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="11be0-106">GetByResourceIdParameterSet</span></span>
```
Get-AzPublicIpPrefix -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11be0-107">描述</span><span class="sxs-lookup"><span data-stu-id="11be0-107">DESCRIPTION</span></span>
<span data-ttu-id="11be0-108">**Get-AzPublicIpPrefix** Cmdlet 會取得資源群組中的一或多個公用 IP 首碼。</span><span class="sxs-lookup"><span data-stu-id="11be0-108">The **Get-AzPublicIpPrefix** cmdlet gets one or more public IP prefixes in a resource group.</span></span>

## <span data-ttu-id="11be0-109">例子</span><span class="sxs-lookup"><span data-stu-id="11be0-109">EXAMPLES</span></span>

### <span data-ttu-id="11be0-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="11be0-110">Example 1</span></span>
```powershell
PS C:\> Get-AzPublicIpPrefix -ResourceGroupName myRg -Name myPublicIpPrefix1

Name                   : myPublicIpPrefix1
ResourceGroupName      : myRg
Location               : westus
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRg/providers/Mic
                         rosoft.Network/publicIPPrefixes/myPublicIpPrefix1
Etag                   : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid           : 00000000-0000-0000-0000-000000000000
ProvisioningState      : Succeeded
Tags                   :
PublicIpAddressVersion : IPv4
PrefixLength           : 28
IPPrefix               : xx.xx.xx.xx/xx
IdleTimeoutInMinutes   :
Zones                  : {}
Sku                    : {
                           "Name": "Standard",
                           "Tier":"Regional"
                         }
IpTags                 : []
PublicIpAddresses      : []
```

<span data-ttu-id="11be0-111">此命令會使用 myPublicIpPrefix1 資源群組 myRg 中的公用 IP 首碼資源</span><span class="sxs-lookup"><span data-stu-id="11be0-111">This command gets a public IP prefix resource with myPublicIpPrefix1 in resource group myRg</span></span>

### <span data-ttu-id="11be0-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="11be0-112">Example 2</span></span>
```powershell
PS C:\> Get-AzPublicIpPrefix -Name myPublicIpPrefix*

Name                   : myPublicIpPrefix1
ResourceGroupName      : myRg
Location               : westus
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRg/providers/Mic
                         rosoft.Network/publicIPPrefixes/myPublicIpPrefix1
Etag                   : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid           : 00000000-0000-0000-0000-000000000000
ProvisioningState      : Succeeded
Tags                   :
PublicIpAddressVersion : IPv4
PrefixLength           : 28
IPPrefix               : xx.xx.xx.xx/xx
IdleTimeoutInMinutes   :
Zones                  : {}
Sku                    : {
                           "Name": "Standard",
                           "Tier": "Regional"
                         }
IpTags                 : []
PublicIpAddresses      : []
```

<span data-ttu-id="11be0-113">此命令會獲得以 myPublicIpPrefix 開頭的所有公用 IP 首碼資源。</span><span class="sxs-lookup"><span data-stu-id="11be0-113">This command gets all public IP prefix resources that start with myPublicIpPrefix.</span></span>

## <span data-ttu-id="11be0-114">參數</span><span class="sxs-lookup"><span data-stu-id="11be0-114">PARAMETERS</span></span>

### <span data-ttu-id="11be0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11be0-115">-DefaultProfile</span></span>
<span data-ttu-id="11be0-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="11be0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11be0-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="11be0-117">-Name</span></span>
<span data-ttu-id="11be0-118">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="11be0-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="11be0-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11be0-119">-ResourceGroupName</span></span>
<span data-ttu-id="11be0-120">資源組名。</span><span class="sxs-lookup"><span data-stu-id="11be0-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="11be0-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="11be0-121">-ResourceId</span></span>
<span data-ttu-id="11be0-122">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="11be0-122">The resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11be0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11be0-123">CommonParameters</span></span>
<span data-ttu-id="11be0-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="11be0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11be0-125">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="11be0-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11be0-126">輸入</span><span class="sxs-lookup"><span data-stu-id="11be0-126">INPUTS</span></span>

### <span data-ttu-id="11be0-127">System.String</span><span class="sxs-lookup"><span data-stu-id="11be0-127">System.String</span></span>

## <span data-ttu-id="11be0-128">輸出</span><span class="sxs-lookup"><span data-stu-id="11be0-128">OUTPUTS</span></span>

### <span data-ttu-id="11be0-129">Microsoft.Azure.Commands.Network.models.PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="11be0-129">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="11be0-130">筆記</span><span class="sxs-lookup"><span data-stu-id="11be0-130">NOTES</span></span>

## <span data-ttu-id="11be0-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="11be0-131">RELATED LINKS</span></span>

[<span data-ttu-id="11be0-132">New-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="11be0-132">New-AzPublicIpPrefix</span></span>](./New-AzPublicIpPrefix.md)

[<span data-ttu-id="11be0-133">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="11be0-133">Remove-AzPublicIpPrefix</span></span>](./Remove-AzPublicIpPrefix.md)

[<span data-ttu-id="11be0-134">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="11be0-134">Set-AzPublicIpPrefix</span></span>](./Set-AzPublicIpPrefix.md)
