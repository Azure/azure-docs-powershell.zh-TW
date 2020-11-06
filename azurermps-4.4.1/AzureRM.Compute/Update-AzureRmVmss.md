---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 9EE192A5-4E3F-41ED-A539-8E0A5D5EA4C9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmVmss.md
ms.openlocfilehash: 44022fe8ea12c8f341952bd023aa41bf4ead92c3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450824"
---
# <span data-ttu-id="0a6b9-101">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="0a6b9-101">Update-AzureRmVmss</span></span>

## <span data-ttu-id="0a6b9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0a6b9-102">SYNOPSIS</span></span>
<span data-ttu-id="0a6b9-103">更新 VMSS 的狀態。</span><span class="sxs-lookup"><span data-stu-id="0a6b9-103">Updates the state of a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0a6b9-104">句法</span><span class="sxs-lookup"><span data-stu-id="0a6b9-104">SYNTAX</span></span>

```
Update-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a6b9-105">說明</span><span class="sxs-lookup"><span data-stu-id="0a6b9-105">DESCRIPTION</span></span>
<span data-ttu-id="0a6b9-106">**更新-AzureRmVmss** Cmdlet 會更新虛擬機器縮放集 (VMSS) 的狀態設定為局部 VMSS 物件的狀態。</span><span class="sxs-lookup"><span data-stu-id="0a6b9-106">The **Update-AzureRmVmss** cmdlet updates the state of a Virtual Machine Scale Set (VMSS) to the state of a local VMSS object.</span></span>

## <span data-ttu-id="0a6b9-107">示例</span><span class="sxs-lookup"><span data-stu-id="0a6b9-107">EXAMPLES</span></span>

### <span data-ttu-id="0a6b9-108">範例1：更新 VMSS 的狀態至本機 VMSS 物件的狀態。</span><span class="sxs-lookup"><span data-stu-id="0a6b9-108">Example 1: Update the state of a VMSS to the state of a local VMSS object.</span></span>
```
PS C:\> Update-AzureRmVmss -ResourceGroupName "Group001" -Name "VMSS001" -VirtualMachineScaleSet "LocalVMSS"
```

<span data-ttu-id="0a6b9-109">這個命令會將屬於名為 Group001 之資源群組的名稱 VMSS001 的 VMSS 狀態，更新為名為 LocalVMSS 的本機 VMSS 物件的狀態。</span><span class="sxs-lookup"><span data-stu-id="0a6b9-109">This command updates the state of the VMSS named VMSS001 that belongs to the resource group named Group001 to the state of a local VMSS object named LocalVMSS.</span></span>

## <span data-ttu-id="0a6b9-110">參數</span><span class="sxs-lookup"><span data-stu-id="0a6b9-110">PARAMETERS</span></span>

### <span data-ttu-id="0a6b9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a6b9-111">-DefaultProfile</span></span>
<span data-ttu-id="0a6b9-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0a6b9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a6b9-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a6b9-113">-ResourceGroupName</span></span>
<span data-ttu-id="0a6b9-114">指定 VMSS 所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0a6b9-114">Specifies the name of the resource group the VMSS belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a6b9-115">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="0a6b9-115">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="0a6b9-116">指定本機 VMSS 物件。</span><span class="sxs-lookup"><span data-stu-id="0a6b9-116">Specifies a local VMSS object.</span></span>
<span data-ttu-id="0a6b9-117">若要取得 VMSS 物件，請使用 Get-AzureRmVmss Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0a6b9-117">To obtain a VMSS object, use the Get-AzureRmVmss cmdlet.</span></span>
<span data-ttu-id="0a6b9-118">此虛擬機器物件包含 VMSS 的更新狀態。</span><span class="sxs-lookup"><span data-stu-id="0a6b9-118">This virtual machine object contains the updated state for the VMSS.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0a6b9-119">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="0a6b9-119">-VMScaleSetName</span></span>
<span data-ttu-id="0a6b9-120">指定此 Cmdlet 所建立之 VMSS 的名稱。</span><span class="sxs-lookup"><span data-stu-id="0a6b9-120">Specifies the name of the VMSS that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a6b9-121">-確認</span><span class="sxs-lookup"><span data-stu-id="0a6b9-121">-Confirm</span></span>
<span data-ttu-id="0a6b9-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0a6b9-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a6b9-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a6b9-123">-WhatIf</span></span>
<span data-ttu-id="0a6b9-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0a6b9-124">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="0a6b9-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0a6b9-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a6b9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a6b9-126">CommonParameters</span></span>
<span data-ttu-id="0a6b9-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0a6b9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a6b9-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0a6b9-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a6b9-129">輸入</span><span class="sxs-lookup"><span data-stu-id="0a6b9-129">INPUTS</span></span>

## <span data-ttu-id="0a6b9-130">輸出</span><span class="sxs-lookup"><span data-stu-id="0a6b9-130">OUTPUTS</span></span>

## <span data-ttu-id="0a6b9-131">筆記</span><span class="sxs-lookup"><span data-stu-id="0a6b9-131">NOTES</span></span>

## <span data-ttu-id="0a6b9-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="0a6b9-132">RELATED LINKS</span></span>

[<span data-ttu-id="0a6b9-133">AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="0a6b9-133">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="0a6b9-134">新-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="0a6b9-134">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="0a6b9-135">移除-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="0a6b9-135">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="0a6b9-136">重新開機-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="0a6b9-136">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="0a6b9-137">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="0a6b9-137">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="0a6b9-138">開始-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="0a6b9-138">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="0a6b9-139">停止 AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="0a6b9-139">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)


