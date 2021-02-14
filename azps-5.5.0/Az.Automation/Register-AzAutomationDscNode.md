---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 73E6DF02-7171-481B-966F-DECEC122A602
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/register-azautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Register-AzAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Register-AzAutomationDscNode.md
ms.openlocfilehash: e8367d4e291f3cd08cdb1020375cce1741a679c8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100130098"
---
# <span data-ttu-id="cba51-101">Register-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="cba51-101">Register-AzAutomationDscNode</span></span>

## <span data-ttu-id="cba51-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cba51-102">SYNOPSIS</span></span>
<span data-ttu-id="cba51-103">將運行 Windows OS 的 Azure 虛擬機器註冊為自動化帳戶的 DSC 節點。</span><span class="sxs-lookup"><span data-stu-id="cba51-103">Registers an Azure virtual machine running Windows OS as a DSC node for an Automation account.</span></span>

## <span data-ttu-id="cba51-104">句法</span><span class="sxs-lookup"><span data-stu-id="cba51-104">SYNTAX</span></span>

```
Register-AzAutomationDscNode -AzureVMName <String> [-NodeConfigurationName <String>]
 [-ConfigurationMode <String>] [-ConfigurationModeFrequencyMins <Int32>] [-RefreshFrequencyMins <Int32>]
 [-RebootNodeIfNeeded <Boolean>] [-ActionAfterReboot <String>] [-AllowModuleOverwrite <Boolean>]
 [-AzureVMResourceGroup <String>] [-AzureVMLocation <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cba51-105">說明</span><span class="sxs-lookup"><span data-stu-id="cba51-105">DESCRIPTION</span></span>
<span data-ttu-id="cba51-106">**AzAutomationDscNode** Cmdlet 會在 azure 自動化帳戶中，將 Azure 虛擬機器註冊為所需的 Ap 狀態配置 (DSC) 節點。</span><span class="sxs-lookup"><span data-stu-id="cba51-106">The **Register-AzAutomationDscNode** cmdlet registers an Azure virtual machine as an APS Desired State Configuration (DSC) node in an Azure Automation account.</span></span> <span data-ttu-id="cba51-107">這個 Cmdlet 只會將運行 Windows OS 的虛擬機器寄存器作為帳戶的自動化 DSC 節點。</span><span class="sxs-lookup"><span data-stu-id="cba51-107">This cmdlet will only register VMs running Windows OS as an Automation DSC Node for an account.</span></span>

<span data-ttu-id="cba51-108">如果您需要將節點註冊到不同訂閱中的自動化帳戶，您將需要使用 ARM 範本，而不是 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cba51-108">If you need to register a node to an automation account in a different subscription, you will need to use an ARM template rather than cmdlets.</span></span> <span data-ttu-id="cba51-109">如需詳細資訊，請參閱 Azure 自動化 [檔](https://docs.microsoft.com/en-us/azure/automation/automation-dsc-onboarding#registering-virtual-machines-across-azure-subscriptions) 。</span><span class="sxs-lookup"><span data-stu-id="cba51-109">See the Azure Automation [documentation](https://docs.microsoft.com/en-us/azure/automation/automation-dsc-onboarding#registering-virtual-machines-across-azure-subscriptions) for more details.</span></span>

## <span data-ttu-id="cba51-110">示例</span><span class="sxs-lookup"><span data-stu-id="cba51-110">EXAMPLES</span></span>

### <span data-ttu-id="cba51-111">範例1：將 Azure 虛擬機器註冊為 Azure DSC 節點</span><span class="sxs-lookup"><span data-stu-id="cba51-111">Example 1: Register an Azure virtual machine as an Azure DSC node</span></span>
```
PS C:\>Register-AzAutomationDscNode -AutomationAccountName "Contoso17" -AzureVMName "VirtualMachine01" -ResourceGroupName "ResourceGroup01"-NodeConfigurationName "ContosoConfiguration.webserver"
```

<span data-ttu-id="cba51-112">這個命令會將名為 VirtualMachine01 的 Azure 虛擬機器註冊為名為 Contoso17 的自動化帳戶中的 DSC 節點。</span><span class="sxs-lookup"><span data-stu-id="cba51-112">This command registers the Azure virtual machine named VirtualMachine01 as a DSC node in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="cba51-113">參數</span><span class="sxs-lookup"><span data-stu-id="cba51-113">PARAMETERS</span></span>

### <span data-ttu-id="cba51-114">-ActionAfterReboot</span><span class="sxs-lookup"><span data-stu-id="cba51-114">-ActionAfterReboot</span></span>
<span data-ttu-id="cba51-115">指定虛擬機器重新開機後所採取的動作。</span><span class="sxs-lookup"><span data-stu-id="cba51-115">Specifies the action that the virtual machine takes after it restarts.</span></span>
<span data-ttu-id="cba51-116">有效值為：</span><span class="sxs-lookup"><span data-stu-id="cba51-116">Valid values are:</span></span> 
- <span data-ttu-id="cba51-117">ContinueConfiguration</span><span class="sxs-lookup"><span data-stu-id="cba51-117">ContinueConfiguration</span></span> 
- <span data-ttu-id="cba51-118">StopConfiguration</span><span class="sxs-lookup"><span data-stu-id="cba51-118">StopConfiguration</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: ContinueConfiguration, StopConfiguration

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cba51-119">-AllowModuleOverwrite</span><span class="sxs-lookup"><span data-stu-id="cba51-119">-AllowModuleOverwrite</span></span>
<span data-ttu-id="cba51-120">指定此 DSC 節點從 Azure 自動化 DSC pull 伺服器下載的新設定是否會取代已在目標節點上的現有模組。</span><span class="sxs-lookup"><span data-stu-id="cba51-120">Specifies whether new configurations that this DSC node downloads from the Azure Automation DSC pull server replace the existing modules already on the target node.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cba51-121">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="cba51-121">-AutomationAccountName</span></span>
<span data-ttu-id="cba51-122">指定此 Cmdlet 註冊虛擬機器之自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="cba51-122">Specifies the name of an Automation account in which this cmdlet registers a virtual machine.</span></span>

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

### <span data-ttu-id="cba51-123">-AzureVMLocation</span><span class="sxs-lookup"><span data-stu-id="cba51-123">-AzureVMLocation</span></span>
<span data-ttu-id="cba51-124">Azure VM 位置。</span><span class="sxs-lookup"><span data-stu-id="cba51-124">The Azure VM location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cba51-125">-AzureVMName</span><span class="sxs-lookup"><span data-stu-id="cba51-125">-AzureVMName</span></span>
<span data-ttu-id="cba51-126">要用來註冊以 Azure Automation DSC 進行管理的 Azure 虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="cba51-126">The name of the Azure virtual machine to register for management with Azure Automation DSC.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cba51-127">-AzureVMResourceGroup</span><span class="sxs-lookup"><span data-stu-id="cba51-127">-AzureVMResourceGroup</span></span>
<span data-ttu-id="cba51-128">Azure VM 資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="cba51-128">The Azure VM resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cba51-129">-ConfigurationMode</span><span class="sxs-lookup"><span data-stu-id="cba51-129">-ConfigurationMode</span></span>
<span data-ttu-id="cba51-130">指定 DSC 配置模式。</span><span class="sxs-lookup"><span data-stu-id="cba51-130">Specifies the DSC configuration mode.</span></span>
<span data-ttu-id="cba51-131">有效值為：</span><span class="sxs-lookup"><span data-stu-id="cba51-131">Valid values are:</span></span> 
- <span data-ttu-id="cba51-132">ApplyAndMonitor</span><span class="sxs-lookup"><span data-stu-id="cba51-132">ApplyAndMonitor</span></span> 
- <span data-ttu-id="cba51-133">ApplyAndAutocorrect</span><span class="sxs-lookup"><span data-stu-id="cba51-133">ApplyAndAutocorrect</span></span> 
- <span data-ttu-id="cba51-134">ApplyOnly</span><span class="sxs-lookup"><span data-stu-id="cba51-134">ApplyOnly</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: ApplyAndMonitor, ApplyAndAutocorrect, ApplyOnly

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cba51-135">-ConfigurationModeFrequencyMins</span><span class="sxs-lookup"><span data-stu-id="cba51-135">-ConfigurationModeFrequencyMins</span></span>
<span data-ttu-id="cba51-136">指定 DSC 的背景應用程式嘗試在目標節點上實現目前設定的頻率（以分鐘為單位）。</span><span class="sxs-lookup"><span data-stu-id="cba51-136">Specifies the frequency, in minutes, at which the background application of DSC attempts to implement the current configuration on the target node.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cba51-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cba51-137">-DefaultProfile</span></span>
<span data-ttu-id="cba51-138">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="cba51-138">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cba51-139">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="cba51-139">-NodeConfigurationName</span></span>
<span data-ttu-id="cba51-140">指定此 Cmdlet 設定要從 Azure Automation DSC 納入的虛擬機器的節點配置名稱。</span><span class="sxs-lookup"><span data-stu-id="cba51-140">Specifies the name of the node configuration that this cmdlet configures the virtual machine to pull from Azure Automation DSC.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cba51-141">-RebootNodeIfNeeded</span><span class="sxs-lookup"><span data-stu-id="cba51-141">-RebootNodeIfNeeded</span></span>
<span data-ttu-id="cba51-142">指定是否要視需要重新開機虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="cba51-142">Specifies whether to restart the virtual machine, if needed.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cba51-143">-RefreshFrequencyMins</span><span class="sxs-lookup"><span data-stu-id="cba51-143">-RefreshFrequencyMins</span></span>
<span data-ttu-id="cba51-144">指定「本機 Configuration Manager」聯絡 Azure 自動化 DSC 拉伺服器以下載最新節點設定的頻率（以分鐘為單位）。</span><span class="sxs-lookup"><span data-stu-id="cba51-144">Specifies the frequency, in minutes, at which the local Configuration Manager contacts the Azure Automation DSC pull server to download the latest node configuration.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cba51-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cba51-145">-ResourceGroupName</span></span>
<span data-ttu-id="cba51-146">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="cba51-146">Specifies the name of a resource group.</span></span>
<span data-ttu-id="cba51-147">此 Cmdlet 註冊虛擬機器的自動化帳戶屬於此參數指定的資源群組。</span><span class="sxs-lookup"><span data-stu-id="cba51-147">The Automation account with which this cmdlet registers a virtual machine belongs to the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="cba51-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cba51-148">CommonParameters</span></span>
<span data-ttu-id="cba51-149">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cba51-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cba51-150">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cba51-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cba51-151">輸入</span><span class="sxs-lookup"><span data-stu-id="cba51-151">INPUTS</span></span>

### <span data-ttu-id="cba51-152">System.object</span><span class="sxs-lookup"><span data-stu-id="cba51-152">System.String</span></span>

### <span data-ttu-id="cba51-153">System.object</span><span class="sxs-lookup"><span data-stu-id="cba51-153">System.Int32</span></span>

### <span data-ttu-id="cba51-154">System.object</span><span class="sxs-lookup"><span data-stu-id="cba51-154">System.Boolean</span></span>

## <span data-ttu-id="cba51-155">輸出</span><span class="sxs-lookup"><span data-stu-id="cba51-155">OUTPUTS</span></span>

### <span data-ttu-id="cba51-156">System.void</span><span class="sxs-lookup"><span data-stu-id="cba51-156">System.Void</span></span>

## <span data-ttu-id="cba51-157">筆記</span><span class="sxs-lookup"><span data-stu-id="cba51-157">NOTES</span></span>

## <span data-ttu-id="cba51-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="cba51-158">RELATED LINKS</span></span>

[<span data-ttu-id="cba51-159">AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="cba51-159">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="cba51-160">Set-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="cba51-160">Set-AzAutomationDscNode</span></span>](./Set-AzAutomationDscNode.md)

[<span data-ttu-id="cba51-161">取消註冊-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="cba51-161">Unregister-AzAutomationDscNode</span></span>](./Unregister-AzAutomationDscNode.md)


