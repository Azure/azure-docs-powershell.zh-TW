---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azcustomipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzCustomIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzCustomIpPrefix.md
ms.openlocfilehash: 08df4120e762a7837376af7413504a8fce678230
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98435777"
---
# <span data-ttu-id="e3fd2-101">New-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="e3fd2-101">New-AzCustomIpPrefix</span></span>

## <span data-ttu-id="e3fd2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e3fd2-102">SYNOPSIS</span></span>
<span data-ttu-id="e3fd2-103">建立 CustomIpPrefix 資源</span><span class="sxs-lookup"><span data-stu-id="e3fd2-103">Creates a CustomIpPrefix resource</span></span>

## <span data-ttu-id="e3fd2-104">句法</span><span class="sxs-lookup"><span data-stu-id="e3fd2-104">SYNTAX</span></span>

```
New-AzCustomIpPrefix -Name <String> -ResourceGroupName <String> -Location <String> -Cidr <String>
 [-Zone <String[]>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e3fd2-105">說明</span><span class="sxs-lookup"><span data-stu-id="e3fd2-105">DESCRIPTION</span></span>
<span data-ttu-id="e3fd2-106">**新的-AzCustomIpPrefix** Cmdlet 會建立 CustomIpPrefix 資源。</span><span class="sxs-lookup"><span data-stu-id="e3fd2-106">The **New-AzCustomIpPrefix** cmdlet creates a CustomIpPrefix resource.</span></span>

## <span data-ttu-id="e3fd2-107">示例</span><span class="sxs-lookup"><span data-stu-id="e3fd2-107">EXAMPLES</span></span>

### <span data-ttu-id="e3fd2-108">範例1</span><span class="sxs-lookup"><span data-stu-id="e3fd2-108">Example 1</span></span>
```powershell
PS C:\> $myCustomIpPrefix = New-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName -Cidr 40.40.40.0/24 -Location westus
```

<span data-ttu-id="e3fd2-109">這個命令會建立新的 CustomIpPrefix 資源，名稱 $prefixName 在資源群組 $rgName 中，40.40.40.0/24 的 cidr 是 westus</span><span class="sxs-lookup"><span data-stu-id="e3fd2-109">This command creates a new CustomIpPrefix resource with name $prefixName in resource group $rgName with a cidr of 40.40.40.0/24 in westus</span></span>

## <span data-ttu-id="e3fd2-110">參數</span><span class="sxs-lookup"><span data-stu-id="e3fd2-110">PARAMETERS</span></span>

### <span data-ttu-id="e3fd2-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e3fd2-111">-AsJob</span></span>
<span data-ttu-id="e3fd2-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e3fd2-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e3fd2-113">-Cidr</span><span class="sxs-lookup"><span data-stu-id="e3fd2-113">-Cidr</span></span>
<span data-ttu-id="e3fd2-114">CustomIpPrefix CIDR。</span><span class="sxs-lookup"><span data-stu-id="e3fd2-114">The CustomIpPrefix CIDR.</span></span>

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

### <span data-ttu-id="e3fd2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3fd2-115">-DefaultProfile</span></span>
<span data-ttu-id="e3fd2-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e3fd2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3fd2-117">-位置</span><span class="sxs-lookup"><span data-stu-id="e3fd2-117">-Location</span></span>
<span data-ttu-id="e3fd2-118">CustomIpPrefix 位置。</span><span class="sxs-lookup"><span data-stu-id="e3fd2-118">The CustomIpPrefix location.</span></span>

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

### <span data-ttu-id="e3fd2-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="e3fd2-119">-Name</span></span>
<span data-ttu-id="e3fd2-120">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="e3fd2-120">The resource name.</span></span>

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

### <span data-ttu-id="e3fd2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3fd2-121">-ResourceGroupName</span></span>
<span data-ttu-id="e3fd2-122">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e3fd2-122">The resource group name.</span></span>

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

### <span data-ttu-id="e3fd2-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="e3fd2-123">-Tag</span></span>
<span data-ttu-id="e3fd2-124">代表資源標記的 hashtable。</span><span class="sxs-lookup"><span data-stu-id="e3fd2-124">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="e3fd2-125">-Zone</span><span class="sxs-lookup"><span data-stu-id="e3fd2-125">-Zone</span></span>
<span data-ttu-id="e3fd2-126">代表資源所分派的 IP 必須來自的可用性區域清單。</span><span class="sxs-lookup"><span data-stu-id="e3fd2-126">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="e3fd2-127">-確認</span><span class="sxs-lookup"><span data-stu-id="e3fd2-127">-Confirm</span></span>
<span data-ttu-id="e3fd2-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e3fd2-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3fd2-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3fd2-129">-WhatIf</span></span>
<span data-ttu-id="e3fd2-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e3fd2-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3fd2-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e3fd2-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3fd2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3fd2-132">CommonParameters</span></span>
<span data-ttu-id="e3fd2-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e3fd2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3fd2-134">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e3fd2-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3fd2-135">輸入</span><span class="sxs-lookup"><span data-stu-id="e3fd2-135">INPUTS</span></span>

### <span data-ttu-id="e3fd2-136">System.object</span><span class="sxs-lookup"><span data-stu-id="e3fd2-136">System.String</span></span>

### <span data-ttu-id="e3fd2-137">System.object []</span><span class="sxs-lookup"><span data-stu-id="e3fd2-137">System.String[]</span></span>

### <span data-ttu-id="e3fd2-138">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e3fd2-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e3fd2-139">輸出</span><span class="sxs-lookup"><span data-stu-id="e3fd2-139">OUTPUTS</span></span>

### <span data-ttu-id="e3fd2-140">PSCustomIpPrefix 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e3fd2-140">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

## <span data-ttu-id="e3fd2-141">筆記</span><span class="sxs-lookup"><span data-stu-id="e3fd2-141">NOTES</span></span>

## <span data-ttu-id="e3fd2-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="e3fd2-142">RELATED LINKS</span></span>

[<span data-ttu-id="e3fd2-143">AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="e3fd2-143">Get-AzCustomIpPrefix</span></span>](./Get-AzCustomIpPrefix.md)

[<span data-ttu-id="e3fd2-144">移除-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="e3fd2-144">Remove-AzCustomIpPrefix</span></span>](./Remove-AzCustomIpPrefix.md)

[<span data-ttu-id="e3fd2-145">更新-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="e3fd2-145">Update-AzCustomIpPrefix</span></span>](./Update-AzCustomIpPrefix.md)