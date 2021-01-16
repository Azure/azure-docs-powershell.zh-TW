---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHost.md
ms.openlocfilehash: 0d3f3a34257ad32c8b606b99c3f7170fb15684b0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98282919"
---
# <span data-ttu-id="06d21-101">Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="06d21-101">Remove-AzHost</span></span>

## <span data-ttu-id="06d21-102">摘要</span><span class="sxs-lookup"><span data-stu-id="06d21-102">SYNOPSIS</span></span>
<span data-ttu-id="06d21-103">移除主機。</span><span class="sxs-lookup"><span data-stu-id="06d21-103">Removes a host.</span></span>

## <span data-ttu-id="06d21-104">句法</span><span class="sxs-lookup"><span data-stu-id="06d21-104">SYNTAX</span></span>

### <span data-ttu-id="06d21-105">DefaultParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="06d21-105">DefaultParameter (Default)</span></span>
```
Remove-AzHost [-ResourceGroupName] <String> [-HostGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06d21-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="06d21-106">ResourceIdParameter</span></span>
```
Remove-AzHost [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="06d21-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="06d21-107">ObjectParameter</span></span>
```
Remove-AzHost [-InputObject] <PSHost> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="06d21-108">說明</span><span class="sxs-lookup"><span data-stu-id="06d21-108">DESCRIPTION</span></span>
<span data-ttu-id="06d21-109">這個 Cmdlet 會刪除主機</span><span class="sxs-lookup"><span data-stu-id="06d21-109">This cmdlet will delete a Host</span></span>

## <span data-ttu-id="06d21-110">示例</span><span class="sxs-lookup"><span data-stu-id="06d21-110">EXAMPLES</span></span>

### <span data-ttu-id="06d21-111">範例1</span><span class="sxs-lookup"><span data-stu-id="06d21-111">Example 1</span></span>
```
PS C:\> Get-AzHost -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName -Name $hostName | Remove-AzHost
```

<span data-ttu-id="06d21-112">這個命令會取得並移除指定的主機。</span><span class="sxs-lookup"><span data-stu-id="06d21-112">This command gets and removes the given host.</span></span>

### <span data-ttu-id="06d21-113">範例2</span><span class="sxs-lookup"><span data-stu-id="06d21-113">Example 2</span></span>
```
PS C:\> Remove-AzHost -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName -Name $hostName
```

<span data-ttu-id="06d21-114">這個命令會移除指定的主機。</span><span class="sxs-lookup"><span data-stu-id="06d21-114">This command removes the given host.</span></span>

## <span data-ttu-id="06d21-115">參數</span><span class="sxs-lookup"><span data-stu-id="06d21-115">PARAMETERS</span></span>

### <span data-ttu-id="06d21-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="06d21-116">-AsJob</span></span>
<span data-ttu-id="06d21-117">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="06d21-117">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06d21-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06d21-118">-DefaultProfile</span></span>
<span data-ttu-id="06d21-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="06d21-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06d21-120">-HostGroupName</span><span class="sxs-lookup"><span data-stu-id="06d21-120">-HostGroupName</span></span>
<span data-ttu-id="06d21-121">主機群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="06d21-121">The name of the host group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06d21-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="06d21-122">-InputObject</span></span>
<span data-ttu-id="06d21-123">主機的本機物件。</span><span class="sxs-lookup"><span data-stu-id="06d21-123">The local object of the host.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSHost
Parameter Sets: ObjectParameter
Aliases: Host

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="06d21-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="06d21-124">-Name</span></span>
<span data-ttu-id="06d21-125">主機的名稱。</span><span class="sxs-lookup"><span data-stu-id="06d21-125">The name of the host.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: HostName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06d21-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06d21-126">-ResourceGroupName</span></span>
<span data-ttu-id="06d21-127">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="06d21-127">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06d21-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="06d21-128">-ResourceId</span></span>
<span data-ttu-id="06d21-129">資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="06d21-129">The ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06d21-130">-確認</span><span class="sxs-lookup"><span data-stu-id="06d21-130">-Confirm</span></span>
<span data-ttu-id="06d21-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="06d21-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06d21-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06d21-132">-WhatIf</span></span>
<span data-ttu-id="06d21-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="06d21-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06d21-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="06d21-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06d21-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06d21-135">CommonParameters</span></span>
<span data-ttu-id="06d21-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="06d21-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06d21-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="06d21-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06d21-138">輸入</span><span class="sxs-lookup"><span data-stu-id="06d21-138">INPUTS</span></span>

### <span data-ttu-id="06d21-139">System.object</span><span class="sxs-lookup"><span data-stu-id="06d21-139">System.String</span></span>

### <span data-ttu-id="06d21-140">PSHost 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="06d21-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSHost</span></span>

## <span data-ttu-id="06d21-141">輸出</span><span class="sxs-lookup"><span data-stu-id="06d21-141">OUTPUTS</span></span>

### <span data-ttu-id="06d21-142">PSOperationStatusResponse 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="06d21-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="06d21-143">筆記</span><span class="sxs-lookup"><span data-stu-id="06d21-143">NOTES</span></span>

## <span data-ttu-id="06d21-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="06d21-144">RELATED LINKS</span></span>
