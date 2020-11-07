---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7B3259CD-079D-4E07-8608-F818522EE7CF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/start-azurermvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Start-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Start-AzureRmVM.md
ms.openlocfilehash: 121d9353baaa10058e101d3f8a7d398f345052ff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625330"
---
# <span data-ttu-id="a8e73-101">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a8e73-101">Start-AzureRmVM</span></span>

## <span data-ttu-id="a8e73-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a8e73-102">SYNOPSIS</span></span>
<span data-ttu-id="a8e73-103">啟動 Azure 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="a8e73-103">Starts an Azure virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8e73-104">句法</span><span class="sxs-lookup"><span data-stu-id="a8e73-104">SYNTAX</span></span>

### <span data-ttu-id="a8e73-105">ResourceGroupNameParameterSetName (預設) </span><span class="sxs-lookup"><span data-stu-id="a8e73-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Start-AzureRmVM [-Name] <String> [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8e73-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="a8e73-106">IdParameterSetName</span></span>
```
Start-AzureRmVM [-Name] <String> [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8e73-107">說明</span><span class="sxs-lookup"><span data-stu-id="a8e73-107">DESCRIPTION</span></span>
<span data-ttu-id="a8e73-108">**AzureRmVM** Cmdlet 會啟動 Azure 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="a8e73-108">The **Start-AzureRmVM** cmdlet starts an Azure virtual machine.</span></span>

## <span data-ttu-id="a8e73-109">示例</span><span class="sxs-lookup"><span data-stu-id="a8e73-109">EXAMPLES</span></span>

### <span data-ttu-id="a8e73-110">範例1：啟動虛擬機器</span><span class="sxs-lookup"><span data-stu-id="a8e73-110">Example 1: Start a virtual machine</span></span>
```
PS C:\> Start-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="a8e73-111">這個命令會在 ResourceGroup11 中啟動名為 VirtualMachine07 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="a8e73-111">This command starts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="a8e73-112">參數</span><span class="sxs-lookup"><span data-stu-id="a8e73-112">PARAMETERS</span></span>

### <span data-ttu-id="a8e73-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a8e73-113">-AsJob</span></span>
<span data-ttu-id="a8e73-114">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="a8e73-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="a8e73-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8e73-115">-DefaultProfile</span></span>
<span data-ttu-id="a8e73-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a8e73-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a8e73-117">-識別碼</span><span class="sxs-lookup"><span data-stu-id="a8e73-117">-Id</span></span>
<span data-ttu-id="a8e73-118">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a8e73-118">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8e73-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="a8e73-119">-Name</span></span>
<span data-ttu-id="a8e73-120">虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="a8e73-120">The virtual machine name.</span></span>

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

### <span data-ttu-id="a8e73-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8e73-121">-ResourceGroupName</span></span>
<span data-ttu-id="a8e73-122">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a8e73-122">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8e73-123">-確認</span><span class="sxs-lookup"><span data-stu-id="a8e73-123">-Confirm</span></span>
<span data-ttu-id="a8e73-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a8e73-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8e73-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8e73-125">-WhatIf</span></span>
<span data-ttu-id="a8e73-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a8e73-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a8e73-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a8e73-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8e73-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8e73-128">CommonParameters</span></span>
<span data-ttu-id="a8e73-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a8e73-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8e73-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a8e73-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8e73-131">輸入</span><span class="sxs-lookup"><span data-stu-id="a8e73-131">INPUTS</span></span>

### <span data-ttu-id="a8e73-132">System.object</span><span class="sxs-lookup"><span data-stu-id="a8e73-132">System.String</span></span>

## <span data-ttu-id="a8e73-133">輸出</span><span class="sxs-lookup"><span data-stu-id="a8e73-133">OUTPUTS</span></span>

### <span data-ttu-id="a8e73-134">PSComputeLongRunningOperation 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="a8e73-134">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="a8e73-135">筆記</span><span class="sxs-lookup"><span data-stu-id="a8e73-135">NOTES</span></span>

## <span data-ttu-id="a8e73-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="a8e73-136">RELATED LINKS</span></span>

[<span data-ttu-id="a8e73-137">AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a8e73-137">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="a8e73-138">新-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a8e73-138">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="a8e73-139">移除-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a8e73-139">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="a8e73-140">重新開機-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a8e73-140">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="a8e73-141">停止 AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a8e73-141">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="a8e73-142">更新-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a8e73-142">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


