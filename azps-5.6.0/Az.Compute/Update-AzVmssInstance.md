---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: E8C9D68E-7C68-43D0-B348-72E9713CB99F
online version: https://docs.microsoft.com/powershell/module/az.compute/update-azvmssinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmssInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmssInstance.md
ms.openlocfilehash: ed0ad08d94cbc67832b6a0dbb85882bd18692d5c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912437"
---
# <span data-ttu-id="90e64-101">Update-AzVmssInstance</span><span class="sxs-lookup"><span data-stu-id="90e64-101">Update-AzVmssInstance</span></span>

## <span data-ttu-id="90e64-102">簡介</span><span class="sxs-lookup"><span data-stu-id="90e64-102">SYNOPSIS</span></span>
<span data-ttu-id="90e64-103">開始手動升級 VMSS 實例。</span><span class="sxs-lookup"><span data-stu-id="90e64-103">Starts a manual upgrade of the VMSS instance.</span></span>

## <span data-ttu-id="90e64-104">語法</span><span class="sxs-lookup"><span data-stu-id="90e64-104">SYNTAX</span></span>

```
Update-AzVmssInstance [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90e64-105">描述</span><span class="sxs-lookup"><span data-stu-id="90e64-105">DESCRIPTION</span></span>
<span data-ttu-id="90e64-106">此Update-AzVmssInstance Cmdlet 會開始手動升級指定的虛擬機器縮放集 (VMSS) 實例。</span><span class="sxs-lookup"><span data-stu-id="90e64-106">The Update-AzVmssInstance cmdlet starts a manual upgrade of the specified Virtual Machine Scale Set (VMSS) instance.</span></span>
<span data-ttu-id="90e64-107">當 VMSS 縮放集上的升級政策設定為手動時，就會使用這個選項。</span><span class="sxs-lookup"><span data-stu-id="90e64-107">This is used when the upgrade policy on the VMSS Scale Set is set to manual.</span></span>

## <span data-ttu-id="90e64-108">例子</span><span class="sxs-lookup"><span data-stu-id="90e64-108">EXAMPLES</span></span>

### <span data-ttu-id="90e64-109">範例 1：開始升級 VMSS 實例</span><span class="sxs-lookup"><span data-stu-id="90e64-109">Example 1: Start an upgrade of the VMSS instance</span></span>
```
PS C:\> Update-AzVmssInstance -ResourceGroupName "Group011" -VMScaleSetName "VMScaleSet001" -InstanceId "0"
```

<span data-ttu-id="90e64-110">此命令會啟動名為 VMScaleSet001 的 VMSS 升級，其實例識別碼為 0。</span><span class="sxs-lookup"><span data-stu-id="90e64-110">This command starts an upgrade of the VMSS named VMScaleSet001 that has the instance ID of 0.</span></span>

## <span data-ttu-id="90e64-111">參數</span><span class="sxs-lookup"><span data-stu-id="90e64-111">PARAMETERS</span></span>

### <span data-ttu-id="90e64-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="90e64-112">-AsJob</span></span>
<span data-ttu-id="90e64-113">在背景中執行 Cmdlet 並返回工作以追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="90e64-113">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="90e64-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90e64-114">-DefaultProfile</span></span>
<span data-ttu-id="90e64-115">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="90e64-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90e64-116">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="90e64-116">-InstanceId</span></span>
<span data-ttu-id="90e64-117">指定要升級之實例的識別碼或識別碼，做為字串陣列。</span><span class="sxs-lookup"><span data-stu-id="90e64-117">Specifies, as a string array, the ID or IDs of the instance to upgrade.</span></span>

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

### <span data-ttu-id="90e64-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90e64-118">-ResourceGroupName</span></span>
<span data-ttu-id="90e64-119">指定 VMSS 資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="90e64-119">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="90e64-120">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="90e64-120">-VMScaleSetName</span></span>
<span data-ttu-id="90e64-121">指定此 Cmdlet 升級的 VMSS 實例名稱。</span><span class="sxs-lookup"><span data-stu-id="90e64-121">Specifies the name of the VMSS instance that this cmdlet upgrades.</span></span>

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

### <span data-ttu-id="90e64-122">-確認</span><span class="sxs-lookup"><span data-stu-id="90e64-122">-Confirm</span></span>
<span data-ttu-id="90e64-123">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="90e64-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90e64-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90e64-124">-WhatIf</span></span>
<span data-ttu-id="90e64-125">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="90e64-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90e64-126">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="90e64-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90e64-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90e64-127">CommonParameters</span></span>
<span data-ttu-id="90e64-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="90e64-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90e64-129">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="90e64-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90e64-130">輸入</span><span class="sxs-lookup"><span data-stu-id="90e64-130">INPUTS</span></span>

### <span data-ttu-id="90e64-131">System.String</span><span class="sxs-lookup"><span data-stu-id="90e64-131">System.String</span></span>

### <span data-ttu-id="90e64-132">System.String[]</span><span class="sxs-lookup"><span data-stu-id="90e64-132">System.String[]</span></span>

## <span data-ttu-id="90e64-133">輸出</span><span class="sxs-lookup"><span data-stu-id="90e64-133">OUTPUTS</span></span>

### <span data-ttu-id="90e64-134">Microsoft.Azure.Commands.Compute.Automation.models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="90e64-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="90e64-135">筆記</span><span class="sxs-lookup"><span data-stu-id="90e64-135">NOTES</span></span>

## <span data-ttu-id="90e64-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="90e64-136">RELATED LINKS</span></span>

[<span data-ttu-id="90e64-137">Update-AzEvss</span><span class="sxs-lookup"><span data-stu-id="90e64-137">Update-AzVmss</span></span>](./Update-AzVmss.md)


