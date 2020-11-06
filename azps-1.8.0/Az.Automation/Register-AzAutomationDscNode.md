---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 73E6DF02-7171-481B-966F-DECEC122A602
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/register-azautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Register-AzAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Register-AzAutomationDscNode.md
ms.openlocfilehash: 5dc2682597be6f05a65bafc38424139e9707578f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622994"
---
# <span data-ttu-id="8fa60-101">Register-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="8fa60-101">Register-AzAutomationDscNode</span></span>

## <span data-ttu-id="8fa60-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8fa60-102">SYNOPSIS</span></span>
<span data-ttu-id="8fa60-103">將 Azure 虛擬機器註冊為自動化帳戶的 DSC 節點。</span><span class="sxs-lookup"><span data-stu-id="8fa60-103">Registers an Azure virtual machine as a DSC node for an Automation account.</span></span>

## <span data-ttu-id="8fa60-104">句法</span><span class="sxs-lookup"><span data-stu-id="8fa60-104">SYNTAX</span></span>

```
Register-AzAutomationDscNode -AzureVMName <String> [-NodeConfigurationName <String>]
 [-ConfigurationMode <String>] [-ConfigurationModeFrequencyMins <Int32>] [-RefreshFrequencyMins <Int32>]
 [-RebootNodeIfNeeded <Boolean>] [-ActionAfterReboot <String>] [-AllowModuleOverwrite <Boolean>]
 [-AzureVMResourceGroup <String>] [-AzureVMLocation <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8fa60-105">說明</span><span class="sxs-lookup"><span data-stu-id="8fa60-105">DESCRIPTION</span></span>
<span data-ttu-id="8fa60-106">**AzAutomationDscNode** Cmdlet 會在 azure 自動化帳戶中，將 Azure 虛擬機器註冊為所需的 Ap 狀態配置 (DSC) 節點。</span><span class="sxs-lookup"><span data-stu-id="8fa60-106">The **Register-AzAutomationDscNode** cmdlet registers an Azure virtual machine as an APS Desired State Configuration (DSC) node in an Azure Automation account.</span></span>

## <span data-ttu-id="8fa60-107">示例</span><span class="sxs-lookup"><span data-stu-id="8fa60-107">EXAMPLES</span></span>

### <span data-ttu-id="8fa60-108">範例1：將 Azure 虛擬機器註冊為 Azure DSC 節點</span><span class="sxs-lookup"><span data-stu-id="8fa60-108">Example 1: Register an Azure virtual machine as an Azure DSC node</span></span>
```
PS C:\>Register-AzAutomationDscNode -AutomationAccountName "Contoso17" -AzVMName "VirtualMachine01" -ResourceGroupName "ResourceGroup01"-NodeConfigurationName "ContosoConfiguration.webserver"
```

<span data-ttu-id="8fa60-109">這個命令會將名為 VirtualMachine01 的 Azure 虛擬機器註冊為名為 Contoso17 的自動化帳戶中的 DSC 節點。</span><span class="sxs-lookup"><span data-stu-id="8fa60-109">This command registers the Azure virtual machine named VirtualMachine01 as a DSC node in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="8fa60-110">參數</span><span class="sxs-lookup"><span data-stu-id="8fa60-110">PARAMETERS</span></span>

### <span data-ttu-id="8fa60-111">-ActionAfterReboot</span><span class="sxs-lookup"><span data-stu-id="8fa60-111">-ActionAfterReboot</span></span>
<span data-ttu-id="8fa60-112">指定虛擬機器重新開機後所採取的動作。</span><span class="sxs-lookup"><span data-stu-id="8fa60-112">Specifies the action that the virtual machine takes after it restarts.</span></span>
<span data-ttu-id="8fa60-113">有效值為：</span><span class="sxs-lookup"><span data-stu-id="8fa60-113">Valid values are:</span></span> 
- <span data-ttu-id="8fa60-114">ContinueConfiguration</span><span class="sxs-lookup"><span data-stu-id="8fa60-114">ContinueConfiguration</span></span> 
- <span data-ttu-id="8fa60-115">StopConfiguration</span><span class="sxs-lookup"><span data-stu-id="8fa60-115">StopConfiguration</span></span>

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

### <span data-ttu-id="8fa60-116">-AllowModuleOverwrite</span><span class="sxs-lookup"><span data-stu-id="8fa60-116">-AllowModuleOverwrite</span></span>
<span data-ttu-id="8fa60-117">指定此 DSC 節點從 Azure 自動化 DSC pull 伺服器下載的新設定是否會取代已在目標節點上的現有模組。</span><span class="sxs-lookup"><span data-stu-id="8fa60-117">Specifies whether new configurations that this DSC node downloads from the Azure Automation DSC pull server replace the existing modules already on the target node.</span></span>

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

### <span data-ttu-id="8fa60-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="8fa60-118">-AutomationAccountName</span></span>
<span data-ttu-id="8fa60-119">指定此 Cmdlet 註冊虛擬機器之自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="8fa60-119">Specifies the name of an Automation account in which this cmdlet registers a virtual machine.</span></span>

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

### <span data-ttu-id="8fa60-120">-AzureVMLocation</span><span class="sxs-lookup"><span data-stu-id="8fa60-120">-AzureVMLocation</span></span>
<span data-ttu-id="8fa60-121">Azure VM 位置。</span><span class="sxs-lookup"><span data-stu-id="8fa60-121">The Azure VM location.</span></span>

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

### <span data-ttu-id="8fa60-122">-AzureVMName</span><span class="sxs-lookup"><span data-stu-id="8fa60-122">-AzureVMName</span></span>
<span data-ttu-id="8fa60-123">要用來註冊以 Azure Automation DSC 進行管理的 Azure 虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="8fa60-123">The name of the Azure virtual machine to register for management with Azure Automation DSC.</span></span>

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

### <span data-ttu-id="8fa60-124">-AzureVMResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8fa60-124">-AzureVMResourceGroup</span></span>
<span data-ttu-id="8fa60-125">Azure VM 資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="8fa60-125">The Azure VM resource group name.</span></span>

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

### <span data-ttu-id="8fa60-126">-ConfigurationMode</span><span class="sxs-lookup"><span data-stu-id="8fa60-126">-ConfigurationMode</span></span>
<span data-ttu-id="8fa60-127">指定 DSC 配置模式。</span><span class="sxs-lookup"><span data-stu-id="8fa60-127">Specifies the DSC configuration mode.</span></span>
<span data-ttu-id="8fa60-128">有效值為：</span><span class="sxs-lookup"><span data-stu-id="8fa60-128">Valid values are:</span></span> 
- <span data-ttu-id="8fa60-129">ApplyAndMonitor</span><span class="sxs-lookup"><span data-stu-id="8fa60-129">ApplyAndMonitor</span></span> 
- <span data-ttu-id="8fa60-130">ApplyAndAutocorrect</span><span class="sxs-lookup"><span data-stu-id="8fa60-130">ApplyAndAutocorrect</span></span> 
- <span data-ttu-id="8fa60-131">ApplyOnly</span><span class="sxs-lookup"><span data-stu-id="8fa60-131">ApplyOnly</span></span>

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

### <span data-ttu-id="8fa60-132">-ConfigurationModeFrequencyMins</span><span class="sxs-lookup"><span data-stu-id="8fa60-132">-ConfigurationModeFrequencyMins</span></span>
<span data-ttu-id="8fa60-133">指定 DSC 的背景應用程式嘗試在目標節點上實現目前設定的頻率（以分鐘為單位）。</span><span class="sxs-lookup"><span data-stu-id="8fa60-133">Specifies the frequency, in minutes, at which the background application of DSC attempts to implement the current configuration on the target node.</span></span>

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

### <span data-ttu-id="8fa60-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fa60-134">-DefaultProfile</span></span>
<span data-ttu-id="8fa60-135">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="8fa60-135">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8fa60-136">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="8fa60-136">-NodeConfigurationName</span></span>
<span data-ttu-id="8fa60-137">指定此 Cmdlet 設定要從 Azure Automation DSC 納入的虛擬機器的節點配置名稱。</span><span class="sxs-lookup"><span data-stu-id="8fa60-137">Specifies the name of the node configuration that this cmdlet configures the virtual machine to pull from Azure Automation DSC.</span></span>

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

### <span data-ttu-id="8fa60-138">-RebootNodeIfNeeded</span><span class="sxs-lookup"><span data-stu-id="8fa60-138">-RebootNodeIfNeeded</span></span>
<span data-ttu-id="8fa60-139">指定是否要視需要重新開機虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="8fa60-139">Specifies whether to restart the virtual machine, if needed.</span></span>

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

### <span data-ttu-id="8fa60-140">-RefreshFrequencyMins</span><span class="sxs-lookup"><span data-stu-id="8fa60-140">-RefreshFrequencyMins</span></span>
<span data-ttu-id="8fa60-141">指定「本機 Configuration Manager」聯絡 Azure 自動化 DSC 拉伺服器以下載最新節點設定的頻率（以分鐘為單位）。</span><span class="sxs-lookup"><span data-stu-id="8fa60-141">Specifies the frequency, in minutes, at which the local Configuration Manager contacts the Azure Automation DSC pull server to download the latest node configuration.</span></span>

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

### <span data-ttu-id="8fa60-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8fa60-142">-ResourceGroupName</span></span>
<span data-ttu-id="8fa60-143">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8fa60-143">Specifies the name of a resource group.</span></span>
<span data-ttu-id="8fa60-144">此 Cmdlet 註冊虛擬機器的自動化帳戶屬於此參數指定的資源群組。</span><span class="sxs-lookup"><span data-stu-id="8fa60-144">The Automation account with which this cmdlet registers a virtual machine belongs to the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="8fa60-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fa60-145">CommonParameters</span></span>
<span data-ttu-id="8fa60-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8fa60-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fa60-147">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8fa60-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fa60-148">輸入</span><span class="sxs-lookup"><span data-stu-id="8fa60-148">INPUTS</span></span>

### <span data-ttu-id="8fa60-149">System.object</span><span class="sxs-lookup"><span data-stu-id="8fa60-149">System.String</span></span>

### <span data-ttu-id="8fa60-150">System.object</span><span class="sxs-lookup"><span data-stu-id="8fa60-150">System.Int32</span></span>

### <span data-ttu-id="8fa60-151">System.object</span><span class="sxs-lookup"><span data-stu-id="8fa60-151">System.Boolean</span></span>

## <span data-ttu-id="8fa60-152">輸出</span><span class="sxs-lookup"><span data-stu-id="8fa60-152">OUTPUTS</span></span>

### <span data-ttu-id="8fa60-153">System.void</span><span class="sxs-lookup"><span data-stu-id="8fa60-153">System.Void</span></span>

## <span data-ttu-id="8fa60-154">筆記</span><span class="sxs-lookup"><span data-stu-id="8fa60-154">NOTES</span></span>

## <span data-ttu-id="8fa60-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="8fa60-155">RELATED LINKS</span></span>

[<span data-ttu-id="8fa60-156">AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="8fa60-156">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="8fa60-157">Set-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="8fa60-157">Set-AzAutomationDscNode</span></span>](./Set-AzAutomationDscNode.md)

[<span data-ttu-id="8fa60-158">取消註冊-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="8fa60-158">Unregister-AzAutomationDscNode</span></span>](./Unregister-AzAutomationDscNode.md)


