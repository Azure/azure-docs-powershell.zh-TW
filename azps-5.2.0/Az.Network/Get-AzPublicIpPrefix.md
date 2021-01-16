---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPublicIpPrefix.md
ms.openlocfilehash: 567fdda7c4f95a1bcdecab172223608ec78ef1f9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98283012"
---
# <span data-ttu-id="d8f0b-101">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="d8f0b-101">Get-AzPublicIpPrefix</span></span>

## <span data-ttu-id="d8f0b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d8f0b-102">SYNOPSIS</span></span>
<span data-ttu-id="d8f0b-103">取得公用 IP 首碼</span><span class="sxs-lookup"><span data-stu-id="d8f0b-103">Gets a public IP prefix</span></span>

## <span data-ttu-id="d8f0b-104">句法</span><span class="sxs-lookup"><span data-stu-id="d8f0b-104">SYNTAX</span></span>

### <span data-ttu-id="d8f0b-105">ListParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="d8f0b-105">ListParameterSet (Default)</span></span>
```
Get-AzPublicIpPrefix [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d8f0b-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d8f0b-106">GetByResourceIdParameterSet</span></span>
```
Get-AzPublicIpPrefix -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8f0b-107">說明</span><span class="sxs-lookup"><span data-stu-id="d8f0b-107">DESCRIPTION</span></span>
<span data-ttu-id="d8f0b-108">**AzPublicIpPrefix** Cmdlet 會取得資源群組中的一個或多個公用 IP 首碼。</span><span class="sxs-lookup"><span data-stu-id="d8f0b-108">The **Get-AzPublicIpPrefix** cmdlet gets one or more public IP prefixes in a resource group.</span></span>

## <span data-ttu-id="d8f0b-109">示例</span><span class="sxs-lookup"><span data-stu-id="d8f0b-109">EXAMPLES</span></span>

### <span data-ttu-id="d8f0b-110">範例1</span><span class="sxs-lookup"><span data-stu-id="d8f0b-110">Example 1</span></span>
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

<span data-ttu-id="d8f0b-111">這個命令會在資源群組 myRg 中取得含 myPublicIpPrefix1 的公用 IP 首碼資源</span><span class="sxs-lookup"><span data-stu-id="d8f0b-111">This command gets a public IP prefix resource with myPublicIpPrefix1 in resource group myRg</span></span>

### <span data-ttu-id="d8f0b-112">範例2</span><span class="sxs-lookup"><span data-stu-id="d8f0b-112">Example 2</span></span>
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

<span data-ttu-id="d8f0b-113">這個命令會取得所有以 myPublicIpPrefix 開頭的公用 IP 首碼資源。</span><span class="sxs-lookup"><span data-stu-id="d8f0b-113">This command gets all public IP prefix resources that start with myPublicIpPrefix.</span></span>

## <span data-ttu-id="d8f0b-114">參數</span><span class="sxs-lookup"><span data-stu-id="d8f0b-114">PARAMETERS</span></span>

### <span data-ttu-id="d8f0b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8f0b-115">-DefaultProfile</span></span>
<span data-ttu-id="d8f0b-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d8f0b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8f0b-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="d8f0b-117">-Name</span></span>
<span data-ttu-id="d8f0b-118">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="d8f0b-118">The resource name.</span></span>

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

### <span data-ttu-id="d8f0b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8f0b-119">-ResourceGroupName</span></span>
<span data-ttu-id="d8f0b-120">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d8f0b-120">The resource group name.</span></span>

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

### <span data-ttu-id="d8f0b-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d8f0b-121">-ResourceId</span></span>
<span data-ttu-id="d8f0b-122">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="d8f0b-122">The resource Id.</span></span>

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

### <span data-ttu-id="d8f0b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8f0b-123">CommonParameters</span></span>
<span data-ttu-id="d8f0b-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d8f0b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8f0b-125">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d8f0b-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8f0b-126">輸入</span><span class="sxs-lookup"><span data-stu-id="d8f0b-126">INPUTS</span></span>

### <span data-ttu-id="d8f0b-127">System.object</span><span class="sxs-lookup"><span data-stu-id="d8f0b-127">System.String</span></span>

## <span data-ttu-id="d8f0b-128">輸出</span><span class="sxs-lookup"><span data-stu-id="d8f0b-128">OUTPUTS</span></span>

### <span data-ttu-id="d8f0b-129">PSPublicIpPrefix 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="d8f0b-129">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="d8f0b-130">筆記</span><span class="sxs-lookup"><span data-stu-id="d8f0b-130">NOTES</span></span>

## <span data-ttu-id="d8f0b-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="d8f0b-131">RELATED LINKS</span></span>

[<span data-ttu-id="d8f0b-132">新-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="d8f0b-132">New-AzPublicIpPrefix</span></span>](./New-AzPublicIpPrefix.md)

[<span data-ttu-id="d8f0b-133">移除-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="d8f0b-133">Remove-AzPublicIpPrefix</span></span>](./Remove-AzPublicIpPrefix.md)

[<span data-ttu-id="d8f0b-134">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="d8f0b-134">Set-AzPublicIpPrefix</span></span>](./Set-AzPublicIpPrefix.md)
