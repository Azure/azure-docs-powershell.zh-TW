---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 7F7D1F05-617C-4EC5-8FF5-D816E9148841
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Start-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Start-AzureRmVmss.md
ms.openlocfilehash: 4c1bc282b4a5aa0bf8c324ec523b5c823ce3cd14
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449918"
---
# <span data-ttu-id="c60cc-101">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c60cc-101">Start-AzureRmVmss</span></span>

## <span data-ttu-id="c60cc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c60cc-102">SYNOPSIS</span></span>
<span data-ttu-id="c60cc-103">在 VMSS 中啟動 VMSS 或一組虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="c60cc-103">Starts the VMSS or a set of virtual machines within the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c60cc-104">句法</span><span class="sxs-lookup"><span data-stu-id="c60cc-104">SYNTAX</span></span>

```
Start-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c60cc-105">說明</span><span class="sxs-lookup"><span data-stu-id="c60cc-105">DESCRIPTION</span></span>
<span data-ttu-id="c60cc-106">**AzureRmVmss** Cmdlet 會啟動虛擬機器縮放集 (VMSS) 或一組虛擬機器中的所有虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="c60cc-106">The **Start-AzureRmVmss** cmdlet starts all the virtual machines within the Virtual Machine Scale Set (VMSS) or a set of virtual machines.</span></span>
<span data-ttu-id="c60cc-107">您可以使用 *InstanceId* 參數來選取一組虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="c60cc-107">You can use the *InstanceId* parameter to select a set of virtual machines.</span></span>

## <span data-ttu-id="c60cc-108">示例</span><span class="sxs-lookup"><span data-stu-id="c60cc-108">EXAMPLES</span></span>

### <span data-ttu-id="c60cc-109">範例1：在 VMSS 中啟動一組特定的虛擬機器</span><span class="sxs-lookup"><span data-stu-id="c60cc-109">Example 1: Start a specific set of virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzureRmVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"-InstanceId "0", "1"
```

<span data-ttu-id="c60cc-110">這個命令會啟動由屬於名為 ContosoVMSS 之 VMSS 的實例識別碼字串陣列所指定的一組特定虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="c60cc-110">This command starts a specific set of virtual machines specified by the instance ID string array that belong to the VMSS named ContosoVMSS.</span></span>

### <span data-ttu-id="c60cc-111">範例2：啟動 VMSS 中的所有虛擬機器</span><span class="sxs-lookup"><span data-stu-id="c60cc-111">Example 2: Start all virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzureRmVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="c60cc-112">這個命令會啟動屬於名為 ContosoVMSS 之 VMSS 的所有虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="c60cc-112">This command starts all virtual machines that belong to the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="c60cc-113">參數</span><span class="sxs-lookup"><span data-stu-id="c60cc-113">PARAMETERS</span></span>

### <span data-ttu-id="c60cc-114">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="c60cc-114">-InstanceId</span></span>
<span data-ttu-id="c60cc-115">指定為字串陣列，即 Cmdlet 啟動之實例的識別碼或 Id。</span><span class="sxs-lookup"><span data-stu-id="c60cc-115">Specifies, as a string array, the ID or IDs of the instances that cmdlet starts.</span></span>
<span data-ttu-id="c60cc-116">例如： `-InstanceId "0", "3"`</span><span class="sxs-lookup"><span data-stu-id="c60cc-116">For instance: `-InstanceId "0", "3"`</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c60cc-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c60cc-117">-ResourceGroupName</span></span>
<span data-ttu-id="c60cc-118">指定 VMSS 之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c60cc-118">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="c60cc-119">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="c60cc-119">-VMScaleSetName</span></span>
<span data-ttu-id="c60cc-120">指定此 Cmdlet 啟動虛擬機器的 VMSS 名稱。</span><span class="sxs-lookup"><span data-stu-id="c60cc-120">Specifies the name of the VMSS that this cmdlet starts the virtual machines.</span></span>

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

### <span data-ttu-id="c60cc-121">-確認</span><span class="sxs-lookup"><span data-stu-id="c60cc-121">-Confirm</span></span>
<span data-ttu-id="c60cc-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c60cc-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c60cc-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c60cc-123">-WhatIf</span></span>
<span data-ttu-id="c60cc-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c60cc-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c60cc-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c60cc-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c60cc-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c60cc-126">CommonParameters</span></span>
<span data-ttu-id="c60cc-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c60cc-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c60cc-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c60cc-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c60cc-129">輸入</span><span class="sxs-lookup"><span data-stu-id="c60cc-129">INPUTS</span></span>

### <span data-ttu-id="c60cc-130">所有</span><span class="sxs-lookup"><span data-stu-id="c60cc-130">None</span></span>
<span data-ttu-id="c60cc-131">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="c60cc-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c60cc-132">輸出</span><span class="sxs-lookup"><span data-stu-id="c60cc-132">OUTPUTS</span></span>

###  
<span data-ttu-id="c60cc-133">這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="c60cc-133">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="c60cc-134">筆記</span><span class="sxs-lookup"><span data-stu-id="c60cc-134">NOTES</span></span>

## <span data-ttu-id="c60cc-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="c60cc-135">RELATED LINKS</span></span>

[<span data-ttu-id="c60cc-136">AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c60cc-136">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="c60cc-137">新-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c60cc-137">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="c60cc-138">移除-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c60cc-138">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="c60cc-139">重新開機-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c60cc-139">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="c60cc-140">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c60cc-140">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="c60cc-141">停止 AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c60cc-141">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="c60cc-142">更新-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c60cc-142">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


