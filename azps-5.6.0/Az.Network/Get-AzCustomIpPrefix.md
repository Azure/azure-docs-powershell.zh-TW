---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azcustomipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzCustomIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzCustomIpPrefix.md
ms.openlocfilehash: 49fbc411d8da95ed2ea968224be139d01fc5df0b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913837"
---
# <span data-ttu-id="a9e9d-101">Get-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="a9e9d-101">Get-AzCustomIpPrefix</span></span>

## <span data-ttu-id="a9e9d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a9e9d-102">SYNOPSIS</span></span>
<span data-ttu-id="a9e9d-103">獲得 CustomIpPrefix 資源</span><span class="sxs-lookup"><span data-stu-id="a9e9d-103">Gets a CustomIpPrefix resource</span></span>

## <span data-ttu-id="a9e9d-104">語法</span><span class="sxs-lookup"><span data-stu-id="a9e9d-104">SYNTAX</span></span>

### <span data-ttu-id="a9e9d-105">GetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="a9e9d-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzCustomIpPrefix [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a9e9d-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9e9d-106">GetByResourceIdParameterSet</span></span>
```
Get-AzCustomIpPrefix -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9e9d-107">描述</span><span class="sxs-lookup"><span data-stu-id="a9e9d-107">DESCRIPTION</span></span>
<span data-ttu-id="a9e9d-108">**Get-AzCustomIpPrefix** Cmdlet 取得一或多個 CustomIpPrefixes 指定一組輸入參數</span><span class="sxs-lookup"><span data-stu-id="a9e9d-108">The **Get-AzCustomIpPrefix** cmdlet gets one or more CustomIpPrefixes given the set of input parameters</span></span>

## <span data-ttu-id="a9e9d-109">例子</span><span class="sxs-lookup"><span data-stu-id="a9e9d-109">EXAMPLES</span></span>

### <span data-ttu-id="a9e9d-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="a9e9d-110">Example 1</span></span>
```powershell
PS C:\> Get-AzPublicIpPrefix -ResourceGroupName myRg -Name myCustomIpPrefix

Name                 : myCustomIpPrefix
ResourceGroupName    : myRg
Location             : westus
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/byoip-test-rg/providers/Micro
                       soft.Network/customIPPrefixes/testCustomIpPrefix
Etag                 : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid         : 00000000-0000-0000-0000-000000000000
ProvisioningState    : Succeeded
Tags                 :
Cidr                 : 111.111.111.111/24
CommissionedState    : Provisioning
PublicIpPrefixes     : []
Zones                : {}
```

<span data-ttu-id="a9e9d-111">此命令在資源群組 myRg 中，會獲得名為 myCustomIpPrefix 的 CustomIpPrefix 資源</span><span class="sxs-lookup"><span data-stu-id="a9e9d-111">This command gets a CustomIpPrefix resource named myCustomIpPrefix in resource group myRg</span></span>

## <span data-ttu-id="a9e9d-112">參數</span><span class="sxs-lookup"><span data-stu-id="a9e9d-112">PARAMETERS</span></span>

### <span data-ttu-id="a9e9d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9e9d-113">-DefaultProfile</span></span>
<span data-ttu-id="a9e9d-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a9e9d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9e9d-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="a9e9d-115">-Name</span></span>
<span data-ttu-id="a9e9d-116">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="a9e9d-116">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9e9d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9e9d-117">-ResourceGroupName</span></span>
<span data-ttu-id="a9e9d-118">資源組名。</span><span class="sxs-lookup"><span data-stu-id="a9e9d-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9e9d-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a9e9d-119">-ResourceId</span></span>
<span data-ttu-id="a9e9d-120">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="a9e9d-120">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9e9d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9e9d-121">CommonParameters</span></span>
<span data-ttu-id="a9e9d-122">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a9e9d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9e9d-123">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a9e9d-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9e9d-124">輸入</span><span class="sxs-lookup"><span data-stu-id="a9e9d-124">INPUTS</span></span>

### <span data-ttu-id="a9e9d-125">System.String</span><span class="sxs-lookup"><span data-stu-id="a9e9d-125">System.String</span></span>

## <span data-ttu-id="a9e9d-126">輸出</span><span class="sxs-lookup"><span data-stu-id="a9e9d-126">OUTPUTS</span></span>

### <span data-ttu-id="a9e9d-127">Microsoft.Azure.Commands.Network.models.PSCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="a9e9d-127">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

## <span data-ttu-id="a9e9d-128">筆記</span><span class="sxs-lookup"><span data-stu-id="a9e9d-128">NOTES</span></span>

## <span data-ttu-id="a9e9d-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="a9e9d-129">RELATED LINKS</span></span>

[<span data-ttu-id="a9e9d-130">New-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="a9e9d-130">New-AzCustomIpPrefix</span></span>](./New-AzCustomIpPrefix.md)

[<span data-ttu-id="a9e9d-131">Remove-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="a9e9d-131">Remove-AzCustomIpPrefix</span></span>](./Remove-AzCustomIpPrefix.md)

[<span data-ttu-id="a9e9d-132">Update-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="a9e9d-132">Update-AzCustomIpPrefix</span></span>](./Update-AzCustomIpPrefix.md)