---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: E8C9D68E-7C68-43D0-B348-72E9713CB99F
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvmssinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmssInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmssInstance.md
ms.openlocfilehash: f7adb9ef086b233d44f2e5d9c6eb132669b102e5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98449652"
---
# <span data-ttu-id="ddcb4-101">Update-AzVmssInstance</span><span class="sxs-lookup"><span data-stu-id="ddcb4-101">Update-AzVmssInstance</span></span>

## <span data-ttu-id="ddcb4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ddcb4-102">SYNOPSIS</span></span>
<span data-ttu-id="ddcb4-103">開始手動升級 VMSS 實例。</span><span class="sxs-lookup"><span data-stu-id="ddcb4-103">Starts a manual upgrade of the VMSS instance.</span></span>

## <span data-ttu-id="ddcb4-104">句法</span><span class="sxs-lookup"><span data-stu-id="ddcb4-104">SYNTAX</span></span>

```
Update-AzVmssInstance [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ddcb4-105">說明</span><span class="sxs-lookup"><span data-stu-id="ddcb4-105">DESCRIPTION</span></span>
<span data-ttu-id="ddcb4-106">Update-AzVmssInstance Cmdlet 會啟動手動升級指定的虛擬機器縮放集， (VMSS) 實例。</span><span class="sxs-lookup"><span data-stu-id="ddcb4-106">The Update-AzVmssInstance cmdlet starts a manual upgrade of the specified Virtual Machine Scale Set (VMSS) instance.</span></span>
<span data-ttu-id="ddcb4-107">當 VMSS 縮放設定上的升級原則設定為 [手動] 時，就會使用這種情況。</span><span class="sxs-lookup"><span data-stu-id="ddcb4-107">This is used when the upgrade policy on the VMSS Scale Set is set to manual.</span></span>

## <span data-ttu-id="ddcb4-108">示例</span><span class="sxs-lookup"><span data-stu-id="ddcb4-108">EXAMPLES</span></span>

### <span data-ttu-id="ddcb4-109">範例1：開始升級 VMSS 實例</span><span class="sxs-lookup"><span data-stu-id="ddcb4-109">Example 1: Start an upgrade of the VMSS instance</span></span>
```
PS C:\> Update-AzVmssInstance -ResourceGroupName "Group011" -VMScaleSetName "VMScaleSet001" -InstanceId "0"
```

<span data-ttu-id="ddcb4-110">這個命令會啟動實例識別碼為0的 VMSS 命名 VMScaleSet001。</span><span class="sxs-lookup"><span data-stu-id="ddcb4-110">This command starts an upgrade of the VMSS named VMScaleSet001 that has the instance ID of 0.</span></span>

## <span data-ttu-id="ddcb4-111">參數</span><span class="sxs-lookup"><span data-stu-id="ddcb4-111">PARAMETERS</span></span>

### <span data-ttu-id="ddcb4-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ddcb4-112">-AsJob</span></span>
<span data-ttu-id="ddcb4-113">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="ddcb4-113">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="ddcb4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddcb4-114">-DefaultProfile</span></span>
<span data-ttu-id="ddcb4-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ddcb4-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ddcb4-116">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="ddcb4-116">-InstanceId</span></span>
<span data-ttu-id="ddcb4-117">指定作為字串陣列，即要升級之實例的識別碼或 Id。</span><span class="sxs-lookup"><span data-stu-id="ddcb4-117">Specifies, as a string array, the ID or IDs of the instance to upgrade.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddcb4-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddcb4-118">-ResourceGroupName</span></span>
<span data-ttu-id="ddcb4-119">指定 VMSS 之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ddcb4-119">Specifies the name of the resource group of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddcb4-120">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="ddcb4-120">-VMScaleSetName</span></span>
<span data-ttu-id="ddcb4-121">指定此 Cmdlet 升級之 VMSS 實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="ddcb4-121">Specifies the name of the VMSS instance that this cmdlet upgrades.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddcb4-122">-確認</span><span class="sxs-lookup"><span data-stu-id="ddcb4-122">-Confirm</span></span>
<span data-ttu-id="ddcb4-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ddcb4-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddcb4-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddcb4-124">-WhatIf</span></span>
<span data-ttu-id="ddcb4-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ddcb4-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ddcb4-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ddcb4-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddcb4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddcb4-127">CommonParameters</span></span>
<span data-ttu-id="ddcb4-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ddcb4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddcb4-129">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ddcb4-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddcb4-130">輸入</span><span class="sxs-lookup"><span data-stu-id="ddcb4-130">INPUTS</span></span>

### <span data-ttu-id="ddcb4-131">System.object</span><span class="sxs-lookup"><span data-stu-id="ddcb4-131">System.String</span></span>

### <span data-ttu-id="ddcb4-132">System.object []</span><span class="sxs-lookup"><span data-stu-id="ddcb4-132">System.String[]</span></span>

## <span data-ttu-id="ddcb4-133">輸出</span><span class="sxs-lookup"><span data-stu-id="ddcb4-133">OUTPUTS</span></span>

### <span data-ttu-id="ddcb4-134">PSOperationStatusResponse 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="ddcb4-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="ddcb4-135">筆記</span><span class="sxs-lookup"><span data-stu-id="ddcb4-135">NOTES</span></span>

## <span data-ttu-id="ddcb4-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="ddcb4-136">RELATED LINKS</span></span>

[<span data-ttu-id="ddcb4-137">更新-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ddcb4-137">Update-AzVmss</span></span>](./Update-AzVmss.md)


