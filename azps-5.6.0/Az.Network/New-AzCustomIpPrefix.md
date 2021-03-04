---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azcustomipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzCustomIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzCustomIpPrefix.md
ms.openlocfilehash: 0ac12ba420231d34c5ad278a8fd2a091fe4982da
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904022"
---
# <span data-ttu-id="c7ea9-101">New-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="c7ea9-101">New-AzCustomIpPrefix</span></span>

## <span data-ttu-id="c7ea9-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c7ea9-102">SYNOPSIS</span></span>
<span data-ttu-id="c7ea9-103">建立 CustomIpPrefix 資源</span><span class="sxs-lookup"><span data-stu-id="c7ea9-103">Creates a CustomIpPrefix resource</span></span>

## <span data-ttu-id="c7ea9-104">語法</span><span class="sxs-lookup"><span data-stu-id="c7ea9-104">SYNTAX</span></span>

```
New-AzCustomIpPrefix -Name <String> -ResourceGroupName <String> -Location <String> -Cidr <String>
 [-Zone <String[]>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c7ea9-105">描述</span><span class="sxs-lookup"><span data-stu-id="c7ea9-105">DESCRIPTION</span></span>
<span data-ttu-id="c7ea9-106">**New-AzCustomIpPrefix** Cmdlet 會建立 CustomIpPrefix 資源。</span><span class="sxs-lookup"><span data-stu-id="c7ea9-106">The **New-AzCustomIpPrefix** cmdlet creates a CustomIpPrefix resource.</span></span>

## <span data-ttu-id="c7ea9-107">例子</span><span class="sxs-lookup"><span data-stu-id="c7ea9-107">EXAMPLES</span></span>

### <span data-ttu-id="c7ea9-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="c7ea9-108">Example 1</span></span>
```powershell
PS C:\> $myCustomIpPrefix = New-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName -Cidr 40.40.40.0/24 -Location westus
```

<span data-ttu-id="c7ea9-109">此命令會建立一個新的 CustomIpPrefix 資源，其名稱 $prefixName 在資源群組 $rgName 中具有 40.40.40.0/24 的 cidr in westus</span><span class="sxs-lookup"><span data-stu-id="c7ea9-109">This command creates a new CustomIpPrefix resource with name $prefixName in resource group $rgName with a cidr of 40.40.40.0/24 in westus</span></span>

## <span data-ttu-id="c7ea9-110">參數</span><span class="sxs-lookup"><span data-stu-id="c7ea9-110">PARAMETERS</span></span>

### <span data-ttu-id="c7ea9-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c7ea9-111">-AsJob</span></span>
<span data-ttu-id="c7ea9-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c7ea9-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7ea9-113">-Cidr</span><span class="sxs-lookup"><span data-stu-id="c7ea9-113">-Cidr</span></span>
<span data-ttu-id="c7ea9-114">CustomIpPrefix CIDR。</span><span class="sxs-lookup"><span data-stu-id="c7ea9-114">The CustomIpPrefix CIDR.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7ea9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7ea9-115">-DefaultProfile</span></span>
<span data-ttu-id="c7ea9-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c7ea9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7ea9-117">-位置</span><span class="sxs-lookup"><span data-stu-id="c7ea9-117">-Location</span></span>
<span data-ttu-id="c7ea9-118">CustomIpPrefix 位置。</span><span class="sxs-lookup"><span data-stu-id="c7ea9-118">The CustomIpPrefix location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7ea9-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="c7ea9-119">-Name</span></span>
<span data-ttu-id="c7ea9-120">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="c7ea9-120">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7ea9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7ea9-121">-ResourceGroupName</span></span>
<span data-ttu-id="c7ea9-122">資源組名。</span><span class="sxs-lookup"><span data-stu-id="c7ea9-122">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7ea9-123">-標記</span><span class="sxs-lookup"><span data-stu-id="c7ea9-123">-Tag</span></span>
<span data-ttu-id="c7ea9-124">代表資源標記的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="c7ea9-124">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7ea9-125">-區域</span><span class="sxs-lookup"><span data-stu-id="c7ea9-125">-Zone</span></span>
<span data-ttu-id="c7ea9-126">表示資源需要配置之 IP 的可用性區域清單。</span><span class="sxs-lookup"><span data-stu-id="c7ea9-126">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7ea9-127">-確認</span><span class="sxs-lookup"><span data-stu-id="c7ea9-127">-Confirm</span></span>
<span data-ttu-id="c7ea9-128">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="c7ea9-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7ea9-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7ea9-129">-WhatIf</span></span>
<span data-ttu-id="c7ea9-130">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c7ea9-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7ea9-131">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c7ea9-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7ea9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7ea9-132">CommonParameters</span></span>
<span data-ttu-id="c7ea9-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c7ea9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7ea9-134">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c7ea9-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7ea9-135">輸入</span><span class="sxs-lookup"><span data-stu-id="c7ea9-135">INPUTS</span></span>

### <span data-ttu-id="c7ea9-136">System.String</span><span class="sxs-lookup"><span data-stu-id="c7ea9-136">System.String</span></span>

### <span data-ttu-id="c7ea9-137">System.String[]</span><span class="sxs-lookup"><span data-stu-id="c7ea9-137">System.String[]</span></span>

### <span data-ttu-id="c7ea9-138">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="c7ea9-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="c7ea9-139">輸出</span><span class="sxs-lookup"><span data-stu-id="c7ea9-139">OUTPUTS</span></span>

### <span data-ttu-id="c7ea9-140">Microsoft.Azure.Commands.Network.models.PSCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="c7ea9-140">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

## <span data-ttu-id="c7ea9-141">筆記</span><span class="sxs-lookup"><span data-stu-id="c7ea9-141">NOTES</span></span>

## <span data-ttu-id="c7ea9-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="c7ea9-142">RELATED LINKS</span></span>

[<span data-ttu-id="c7ea9-143">Get-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="c7ea9-143">Get-AzCustomIpPrefix</span></span>](./Get-AzCustomIpPrefix.md)

[<span data-ttu-id="c7ea9-144">Remove-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="c7ea9-144">Remove-AzCustomIpPrefix</span></span>](./Remove-AzCustomIpPrefix.md)

[<span data-ttu-id="c7ea9-145">Update-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="c7ea9-145">Update-AzCustomIpPrefix</span></span>](./Update-AzCustomIpPrefix.md)