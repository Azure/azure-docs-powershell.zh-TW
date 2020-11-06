---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: EF155949-5766-4BC4-9C8A-2B97E8EA032D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Restart-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Restart-AzureRmVM.md
ms.openlocfilehash: 5a848c2e4a13df6a38c67e067531ff8581bd595e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445040"
---
# <span data-ttu-id="98984-101">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="98984-101">Restart-AzureRmVM</span></span>

## <span data-ttu-id="98984-102">摘要</span><span class="sxs-lookup"><span data-stu-id="98984-102">SYNOPSIS</span></span>
<span data-ttu-id="98984-103">重新開機 Azure 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="98984-103">Restarts an Azure virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="98984-104">句法</span><span class="sxs-lookup"><span data-stu-id="98984-104">SYNTAX</span></span>

### <span data-ttu-id="98984-105">RestartResourceGroupNameParameterSetName (預設) </span><span class="sxs-lookup"><span data-stu-id="98984-105">RestartResourceGroupNameParameterSetName (Default)</span></span>
```
Restart-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98984-106">PerformMaintenanceResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="98984-106">PerformMaintenanceResourceGroupNameParameterSetName</span></span>
```
Restart-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-PerformMaintenance]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98984-107">RestartIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="98984-107">RestartIdParameterSetName</span></span>
```
Restart-AzureRmVM [-Id] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98984-108">PerformMaintenanceIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="98984-108">PerformMaintenanceIdParameterSetName</span></span>
```
Restart-AzureRmVM [-Id] <String> [-Name] <String> [-PerformMaintenance]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98984-109">說明</span><span class="sxs-lookup"><span data-stu-id="98984-109">DESCRIPTION</span></span>
<span data-ttu-id="98984-110">**Restart AzureRmVM** Cmdlet 會重新開機 Azure 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="98984-110">The **Restart-AzureRmVM** cmdlet restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="98984-111">示例</span><span class="sxs-lookup"><span data-stu-id="98984-111">EXAMPLES</span></span>

### <span data-ttu-id="98984-112">範例1：重新開機虛擬機器</span><span class="sxs-lookup"><span data-stu-id="98984-112">Example 1: Restart a virtual machine</span></span>
```
PS C:\> Restart-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="98984-113">這個命令會在 ResourceGroup11 中重新開機名為 VirtualMachine07 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="98984-113">This command restarts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="98984-114">參數</span><span class="sxs-lookup"><span data-stu-id="98984-114">PARAMETERS</span></span>

### <span data-ttu-id="98984-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98984-115">-DefaultProfile</span></span>
<span data-ttu-id="98984-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="98984-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="98984-117">-識別碼</span><span class="sxs-lookup"><span data-stu-id="98984-117">-Id</span></span>
<span data-ttu-id="98984-118">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="98984-118">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RestartIdParameterSetName, PerformMaintenanceIdParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98984-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="98984-119">-Name</span></span>
<span data-ttu-id="98984-120">虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="98984-120">The virtual machine name.</span></span>

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

### <span data-ttu-id="98984-121">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="98984-121">-PerformMaintenance</span></span>
<span data-ttu-id="98984-122">執行虛擬機器的維護作業。</span><span class="sxs-lookup"><span data-stu-id="98984-122">To perform the maintenance of virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PerformMaintenanceResourceGroupNameParameterSetName, PerformMaintenanceIdParameterSetName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98984-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98984-123">-ResourceGroupName</span></span>
<span data-ttu-id="98984-124">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="98984-124">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RestartResourceGroupNameParameterSetName, PerformMaintenanceResourceGroupNameParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98984-125">-確認</span><span class="sxs-lookup"><span data-stu-id="98984-125">-Confirm</span></span>
<span data-ttu-id="98984-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="98984-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98984-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98984-127">-WhatIf</span></span>
<span data-ttu-id="98984-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="98984-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="98984-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="98984-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98984-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98984-130">CommonParameters</span></span>
<span data-ttu-id="98984-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="98984-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98984-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="98984-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98984-133">輸入</span><span class="sxs-lookup"><span data-stu-id="98984-133">INPUTS</span></span>

## <span data-ttu-id="98984-134">輸出</span><span class="sxs-lookup"><span data-stu-id="98984-134">OUTPUTS</span></span>

## <span data-ttu-id="98984-135">筆記</span><span class="sxs-lookup"><span data-stu-id="98984-135">NOTES</span></span>

## <span data-ttu-id="98984-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="98984-136">RELATED LINKS</span></span>

[<span data-ttu-id="98984-137">AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="98984-137">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="98984-138">新-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="98984-138">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="98984-139">移除-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="98984-139">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="98984-140">開始-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="98984-140">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="98984-141">停止 AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="98984-141">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="98984-142">更新-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="98984-142">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


