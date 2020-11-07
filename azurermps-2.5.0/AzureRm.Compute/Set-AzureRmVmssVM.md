---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 70AA9747-232E-40F2-845C-35A779F51CD2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmssvm
schema: 2.0.0
ms.openlocfilehash: ffce87e30fb5bffa78cb10a85b1ac8a143deeaad
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93802546"
---
# <span data-ttu-id="b200e-101">Set-AzureRmVmssVM</span><span class="sxs-lookup"><span data-stu-id="b200e-101">Set-AzureRmVmssVM</span></span>

## <span data-ttu-id="b200e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b200e-102">SYNOPSIS</span></span>
<span data-ttu-id="b200e-103">修改 VMSS 實例的狀態。</span><span class="sxs-lookup"><span data-stu-id="b200e-103">Modifies the state of a VMSS instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b200e-104">句法</span><span class="sxs-lookup"><span data-stu-id="b200e-104">SYNTAX</span></span>

### <span data-ttu-id="b200e-105">DefaultParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="b200e-105">DefaultParameter (Default)</span></span>
```
Set-AzureRmVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-Reimage]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b200e-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="b200e-106">FriendMethod</span></span>
```
Set-AzureRmVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-ReimageAll]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b200e-107">說明</span><span class="sxs-lookup"><span data-stu-id="b200e-107">DESCRIPTION</span></span>
<span data-ttu-id="b200e-108">**AzureRmVmssVM** Cmdlet 會修改虛擬機器縮放集 (VMSS) 實例的狀態。</span><span class="sxs-lookup"><span data-stu-id="b200e-108">The **Set-AzureRmVmssVM** cmdlet modifies the state of a Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="b200e-109">示例</span><span class="sxs-lookup"><span data-stu-id="b200e-109">EXAMPLES</span></span>

## <span data-ttu-id="b200e-110">參數</span><span class="sxs-lookup"><span data-stu-id="b200e-110">PARAMETERS</span></span>

### <span data-ttu-id="b200e-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b200e-111">-AsJob</span></span>
<span data-ttu-id="b200e-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b200e-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b200e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b200e-113">-DefaultProfile</span></span>
<span data-ttu-id="b200e-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b200e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b200e-115">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="b200e-115">-InstanceId</span></span>
<span data-ttu-id="b200e-116">指定此 Cmdlet 修改狀態的 VMSS 實例識別碼。</span><span class="sxs-lookup"><span data-stu-id="b200e-116">Specifies the ID of the VMSS instance for which this cmdlet modifies state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b200e-117">-重新映射</span><span class="sxs-lookup"><span data-stu-id="b200e-117">-Reimage</span></span>
<span data-ttu-id="b200e-118">表示此 Cmdlet reimages VMSS 實例。</span><span class="sxs-lookup"><span data-stu-id="b200e-118">Indicates that this cmdlet reimages the VMSS instance.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b200e-119">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="b200e-119">-ReimageAll</span></span>
<span data-ttu-id="b200e-120">表示 Cmdlet reimages VMSS 實例中的所有磁片。</span><span class="sxs-lookup"><span data-stu-id="b200e-120">Indicates that the cmdlet reimages all the disks in the VMSS instance.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b200e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b200e-121">-ResourceGroupName</span></span>
<span data-ttu-id="b200e-122">指定包含 VMSS 實例之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b200e-122">Specifies the name of the resource group that contains the VMSS instance.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b200e-123">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="b200e-123">-VMScaleSetName</span></span>
<span data-ttu-id="b200e-124">指定此 Cmdlet 所修改之 VMSS 實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="b200e-124">Specifies the name of the VMSS instance that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b200e-125">-確認</span><span class="sxs-lookup"><span data-stu-id="b200e-125">-Confirm</span></span>
<span data-ttu-id="b200e-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b200e-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b200e-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b200e-127">-WhatIf</span></span>
<span data-ttu-id="b200e-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b200e-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b200e-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b200e-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b200e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b200e-130">CommonParameters</span></span>
<span data-ttu-id="b200e-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b200e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b200e-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b200e-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b200e-133">輸入</span><span class="sxs-lookup"><span data-stu-id="b200e-133">INPUTS</span></span>

### <span data-ttu-id="b200e-134">所有</span><span class="sxs-lookup"><span data-stu-id="b200e-134">None</span></span>
<span data-ttu-id="b200e-135">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="b200e-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b200e-136">輸出</span><span class="sxs-lookup"><span data-stu-id="b200e-136">OUTPUTS</span></span>

### <span data-ttu-id="b200e-137">PSOperationStatusResponse 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="b200e-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="b200e-138">筆記</span><span class="sxs-lookup"><span data-stu-id="b200e-138">NOTES</span></span>

## <span data-ttu-id="b200e-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="b200e-139">RELATED LINKS</span></span>

[<span data-ttu-id="b200e-140">AzureRmVmssVM</span><span class="sxs-lookup"><span data-stu-id="b200e-140">Get-AzureRmVmssVM</span></span>](./Get-AzureRmVmssVM.md)
