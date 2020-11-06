---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 47F0EE55-78C0-4C71-BD32-C7CB7B200DC3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Restart-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Restart-AzureRmVmss.md
ms.openlocfilehash: 479aaf61169cb09d8561e9f09b05a5852c93b58d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445036"
---
# <span data-ttu-id="35cb6-101">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="35cb6-101">Restart-AzureRmVmss</span></span>

## <span data-ttu-id="35cb6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="35cb6-102">SYNOPSIS</span></span>
<span data-ttu-id="35cb6-103">重新開機 VMSS 或 VMSS 中的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="35cb6-103">Restarts the VMSS or a virtual machine within the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="35cb6-104">句法</span><span class="sxs-lookup"><span data-stu-id="35cb6-104">SYNTAX</span></span>

```
Restart-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35cb6-105">說明</span><span class="sxs-lookup"><span data-stu-id="35cb6-105">DESCRIPTION</span></span>
<span data-ttu-id="35cb6-106">**Restart AzureRmVmss** Cmdlet 會重新開機虛擬機器縮放集 (VMSS) 。</span><span class="sxs-lookup"><span data-stu-id="35cb6-106">The **Restart-AzureRmVmss** cmdlet restarts the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="35cb6-107">這個 Cmdlet 也可以用來在 VMSS 內使用 *InstanceId* 參數重新開機特定的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="35cb6-107">This cmdlet can also be used to restart a specific virtual machine inside the VMSS by using the *InstanceId* parameter.</span></span>

## <span data-ttu-id="35cb6-108">示例</span><span class="sxs-lookup"><span data-stu-id="35cb6-108">EXAMPLES</span></span>

### <span data-ttu-id="35cb6-109">範例1：重新開機 VMSS</span><span class="sxs-lookup"><span data-stu-id="35cb6-109">Example 1: Restart the VMSS</span></span>
```
PS C:\> Restart-AzureRmVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001";
```

<span data-ttu-id="35cb6-110">這個命令會重新開機屬於名為 Group001 之資源群組的名為 VMSS001 的 VMSS。</span><span class="sxs-lookup"><span data-stu-id="35cb6-110">This command restarts the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

### <span data-ttu-id="35cb6-111">範例2：在 VMSS 中重新開機特定的虛擬機器</span><span class="sxs-lookup"><span data-stu-id="35cb6-111">Example 2: Restart a specific virtual machine within the VMSS</span></span>
```
PS C:\> Restart-AzureRmVmss -ResourceGroupName "Group004" -VMScaleSetName "VMSS001" -InstanceId "1"
```

<span data-ttu-id="35cb6-112">這個命令會在屬於名為 Group001 之資源群組的名稱為 VMSS 的 VMSS001 中，重新開機實例識別碼為1的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="35cb6-112">This command restarts a virtual machine that has the instance ID of 1 in the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="35cb6-113">參數</span><span class="sxs-lookup"><span data-stu-id="35cb6-113">PARAMETERS</span></span>

### <span data-ttu-id="35cb6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35cb6-114">-DefaultProfile</span></span>
<span data-ttu-id="35cb6-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="35cb6-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="35cb6-116">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="35cb6-116">-InstanceId</span></span>
<span data-ttu-id="35cb6-117">指定為字串陣列（需要重新開機的實例識別碼）。</span><span class="sxs-lookup"><span data-stu-id="35cb6-117">Specifies, as a string array, the ID of the instances that need restarted.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35cb6-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35cb6-118">-ResourceGroupName</span></span>
<span data-ttu-id="35cb6-119">指定 VMSS 之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="35cb6-119">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="35cb6-120">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="35cb6-120">-VMScaleSetName</span></span>
<span data-ttu-id="35cb6-121">Species 此 Cmdlet 重新開機之 VMSS 的名稱。</span><span class="sxs-lookup"><span data-stu-id="35cb6-121">Species the name of the VMSS that this cmdlet restarts.</span></span>

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

### <span data-ttu-id="35cb6-122">-確認</span><span class="sxs-lookup"><span data-stu-id="35cb6-122">-Confirm</span></span>
<span data-ttu-id="35cb6-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="35cb6-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35cb6-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35cb6-124">-WhatIf</span></span>
<span data-ttu-id="35cb6-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="35cb6-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="35cb6-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="35cb6-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35cb6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35cb6-127">CommonParameters</span></span>
<span data-ttu-id="35cb6-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="35cb6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35cb6-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="35cb6-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35cb6-130">輸入</span><span class="sxs-lookup"><span data-stu-id="35cb6-130">INPUTS</span></span>

## <span data-ttu-id="35cb6-131">輸出</span><span class="sxs-lookup"><span data-stu-id="35cb6-131">OUTPUTS</span></span>

###  
<span data-ttu-id="35cb6-132">這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="35cb6-132">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="35cb6-133">筆記</span><span class="sxs-lookup"><span data-stu-id="35cb6-133">NOTES</span></span>

## <span data-ttu-id="35cb6-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="35cb6-134">RELATED LINKS</span></span>

[<span data-ttu-id="35cb6-135">AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="35cb6-135">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="35cb6-136">新-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="35cb6-136">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="35cb6-137">移除-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="35cb6-137">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="35cb6-138">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="35cb6-138">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="35cb6-139">開始-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="35cb6-139">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="35cb6-140">停止 AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="35cb6-140">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="35cb6-141">更新-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="35cb6-141">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


