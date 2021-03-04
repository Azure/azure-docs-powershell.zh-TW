---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7B3259CD-079D-4E07-8608-F818522EE7CF
online version: https://docs.microsoft.com/powershell/module/az.compute/start-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVM.md
ms.openlocfilehash: daf1a9c738e6e4d0d97a22eedc8355750d15ec72
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915586"
---
# <span data-ttu-id="f0342-101">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="f0342-101">Start-AzVM</span></span>

## <span data-ttu-id="f0342-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f0342-102">SYNOPSIS</span></span>
<span data-ttu-id="f0342-103">啟動 Azure 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="f0342-103">Starts an Azure virtual machine.</span></span>

## <span data-ttu-id="f0342-104">語法</span><span class="sxs-lookup"><span data-stu-id="f0342-104">SYNTAX</span></span>

### <span data-ttu-id="f0342-105">ResourceGroupNameParameterSetName (預設) </span><span class="sxs-lookup"><span data-stu-id="f0342-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Start-AzVM [-Name] <String> [-NoWait] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0342-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="f0342-106">IdParameterSetName</span></span>
```
Start-AzVM [-NoWait] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f0342-107">描述</span><span class="sxs-lookup"><span data-stu-id="f0342-107">DESCRIPTION</span></span>
<span data-ttu-id="f0342-108">**Start-AzMS** Cmdlet 會啟動 Azure 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="f0342-108">The **Start-AzVM** cmdlet starts an Azure virtual machine.</span></span>

## <span data-ttu-id="f0342-109">例子</span><span class="sxs-lookup"><span data-stu-id="f0342-109">EXAMPLES</span></span>

### <span data-ttu-id="f0342-110">範例 1：啟動虛擬機器</span><span class="sxs-lookup"><span data-stu-id="f0342-110">Example 1: Start a virtual machine</span></span>
```
PS C:\> Start-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="f0342-111">此命令會啟動 ResourceGroup11 中名為 VirtualMachine07 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="f0342-111">This command starts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="f0342-112">參數</span><span class="sxs-lookup"><span data-stu-id="f0342-112">PARAMETERS</span></span>

### <span data-ttu-id="f0342-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f0342-113">-AsJob</span></span>
<span data-ttu-id="f0342-114">在背景中執行 Cmdlet 並返回工作以追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="f0342-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="f0342-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0342-115">-DefaultProfile</span></span>
<span data-ttu-id="f0342-116">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f0342-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f0342-117">-Id</span><span class="sxs-lookup"><span data-stu-id="f0342-117">-Id</span></span>
<span data-ttu-id="f0342-118">虛擬機器的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f0342-118">The ID of the virtual machine.</span></span>

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

### <span data-ttu-id="f0342-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="f0342-119">-Name</span></span>
<span data-ttu-id="f0342-120">虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="f0342-120">The virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0342-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="f0342-121">-NoWait</span></span>
<span data-ttu-id="f0342-122">啟動作業，並立即在作業完成之前返回。</span><span class="sxs-lookup"><span data-stu-id="f0342-122">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="f0342-123">若要判斷作業是否成功完成，請使用一些其他機制。</span><span class="sxs-lookup"><span data-stu-id="f0342-123">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="f0342-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0342-124">-ResourceGroupName</span></span>
<span data-ttu-id="f0342-125">指定虛擬機器的資源組名。</span><span class="sxs-lookup"><span data-stu-id="f0342-125">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="f0342-126">-確認</span><span class="sxs-lookup"><span data-stu-id="f0342-126">-Confirm</span></span>
<span data-ttu-id="f0342-127">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="f0342-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0342-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0342-128">-WhatIf</span></span>
<span data-ttu-id="f0342-129">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f0342-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f0342-130">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f0342-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0342-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0342-131">CommonParameters</span></span>
<span data-ttu-id="f0342-132">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f0342-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0342-133">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f0342-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0342-134">輸入</span><span class="sxs-lookup"><span data-stu-id="f0342-134">INPUTS</span></span>

### <span data-ttu-id="f0342-135">System.String</span><span class="sxs-lookup"><span data-stu-id="f0342-135">System.String</span></span>

## <span data-ttu-id="f0342-136">輸出</span><span class="sxs-lookup"><span data-stu-id="f0342-136">OUTPUTS</span></span>

### <span data-ttu-id="f0342-137">Microsoft.Azure.Commands.Compute.models.PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="f0342-137">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="f0342-138">Microsoft.Azure.Commands.Compute.models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="f0342-138">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="f0342-139">筆記</span><span class="sxs-lookup"><span data-stu-id="f0342-139">NOTES</span></span>

## <span data-ttu-id="f0342-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="f0342-140">RELATED LINKS</span></span>

[<span data-ttu-id="f0342-141">Get-AzMS</span><span class="sxs-lookup"><span data-stu-id="f0342-141">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="f0342-142">New-AzMS</span><span class="sxs-lookup"><span data-stu-id="f0342-142">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="f0342-143">Remove-AzMS</span><span class="sxs-lookup"><span data-stu-id="f0342-143">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="f0342-144">Restart-AzMS</span><span class="sxs-lookup"><span data-stu-id="f0342-144">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="f0342-145">Stop-AzMS</span><span class="sxs-lookup"><span data-stu-id="f0342-145">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="f0342-146">Update-AzMS</span><span class="sxs-lookup"><span data-stu-id="f0342-146">Update-AzVM</span></span>](./Update-AzVM.md)


