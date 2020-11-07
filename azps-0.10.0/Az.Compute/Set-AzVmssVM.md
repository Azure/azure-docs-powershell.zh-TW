---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 70AA9747-232E-40F2-845C-35A779F51CD2
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVmssVM.md
ms.openlocfilehash: 8dde17b43de9db13f1f61c909ee8c88b95761751
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794846"
---
# <span data-ttu-id="d78e5-101">Set-AzVmssVM</span><span class="sxs-lookup"><span data-stu-id="d78e5-101">Set-AzVmssVM</span></span>

## <span data-ttu-id="d78e5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d78e5-102">SYNOPSIS</span></span>
<span data-ttu-id="d78e5-103">修改 VMSS 實例的狀態。</span><span class="sxs-lookup"><span data-stu-id="d78e5-103">Modifies the state of a VMSS instance.</span></span>

## <span data-ttu-id="d78e5-104">句法</span><span class="sxs-lookup"><span data-stu-id="d78e5-104">SYNTAX</span></span>

### <span data-ttu-id="d78e5-105">DefaultParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="d78e5-105">DefaultParameter (Default)</span></span>
```
Set-AzVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-Reimage]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d78e5-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="d78e5-106">FriendMethod</span></span>
```
Set-AzVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-ReimageAll]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d78e5-107">說明</span><span class="sxs-lookup"><span data-stu-id="d78e5-107">DESCRIPTION</span></span>
<span data-ttu-id="d78e5-108">**AzVmssVM** Cmdlet 會修改虛擬機器縮放集 (VMSS) 實例的狀態。</span><span class="sxs-lookup"><span data-stu-id="d78e5-108">The **Set-AzVmssVM** cmdlet modifies the state of a Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="d78e5-109">示例</span><span class="sxs-lookup"><span data-stu-id="d78e5-109">EXAMPLES</span></span>

## <span data-ttu-id="d78e5-110">參數</span><span class="sxs-lookup"><span data-stu-id="d78e5-110">PARAMETERS</span></span>

### <span data-ttu-id="d78e5-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d78e5-111">-AsJob</span></span>
<span data-ttu-id="d78e5-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="d78e5-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d78e5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d78e5-113">-DefaultProfile</span></span>
<span data-ttu-id="d78e5-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d78e5-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d78e5-115">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="d78e5-115">-InstanceId</span></span>
<span data-ttu-id="d78e5-116">指定此 Cmdlet 修改狀態的 VMSS 實例識別碼。</span><span class="sxs-lookup"><span data-stu-id="d78e5-116">Specifies the ID of the VMSS instance for which this cmdlet modifies state.</span></span>

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

### <span data-ttu-id="d78e5-117">-重新映射</span><span class="sxs-lookup"><span data-stu-id="d78e5-117">-Reimage</span></span>
<span data-ttu-id="d78e5-118">表示此 Cmdlet reimages VMSS 實例。</span><span class="sxs-lookup"><span data-stu-id="d78e5-118">Indicates that this cmdlet reimages the VMSS instance.</span></span>

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

### <span data-ttu-id="d78e5-119">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="d78e5-119">-ReimageAll</span></span>
<span data-ttu-id="d78e5-120">表示 Cmdlet reimages VMSS 實例中的所有磁片。</span><span class="sxs-lookup"><span data-stu-id="d78e5-120">Indicates that the cmdlet reimages all the disks in the VMSS instance.</span></span>

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

### <span data-ttu-id="d78e5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d78e5-121">-ResourceGroupName</span></span>
<span data-ttu-id="d78e5-122">指定包含 VMSS 實例之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d78e5-122">Specifies the name of the resource group that contains the VMSS instance.</span></span>

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

### <span data-ttu-id="d78e5-123">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="d78e5-123">-VMScaleSetName</span></span>
<span data-ttu-id="d78e5-124">指定此 Cmdlet 所修改之 VMSS 實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="d78e5-124">Specifies the name of the VMSS instance that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="d78e5-125">-確認</span><span class="sxs-lookup"><span data-stu-id="d78e5-125">-Confirm</span></span>
<span data-ttu-id="d78e5-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d78e5-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d78e5-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d78e5-127">-WhatIf</span></span>
<span data-ttu-id="d78e5-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d78e5-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d78e5-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d78e5-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d78e5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d78e5-130">CommonParameters</span></span>
<span data-ttu-id="d78e5-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d78e5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d78e5-132">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d78e5-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d78e5-133">輸入</span><span class="sxs-lookup"><span data-stu-id="d78e5-133">INPUTS</span></span>

### <span data-ttu-id="d78e5-134">所有</span><span class="sxs-lookup"><span data-stu-id="d78e5-134">None</span></span>
<span data-ttu-id="d78e5-135">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="d78e5-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d78e5-136">輸出</span><span class="sxs-lookup"><span data-stu-id="d78e5-136">OUTPUTS</span></span>

### <span data-ttu-id="d78e5-137">PSOperationStatusResponse 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="d78e5-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="d78e5-138">筆記</span><span class="sxs-lookup"><span data-stu-id="d78e5-138">NOTES</span></span>

## <span data-ttu-id="d78e5-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="d78e5-139">RELATED LINKS</span></span>

[<span data-ttu-id="d78e5-140">AzVmssVM</span><span class="sxs-lookup"><span data-stu-id="d78e5-140">Get-AzVmssVM</span></span>](./Get-AzVmssVM.md)
