---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 73E6DF02-7171-481B-966F-DECEC122A602
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Register-AzureRmAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Register-AzureRmAutomationDscNode.md
ms.openlocfilehash: 1a0fd95df118e734ed594cf1efe35eb8f8476f50
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450899"
---
# <span data-ttu-id="9f91c-101">Register-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="9f91c-101">Register-AzureRmAutomationDscNode</span></span>

## <span data-ttu-id="9f91c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9f91c-102">SYNOPSIS</span></span>
<span data-ttu-id="9f91c-103">將 Azure 虛擬機器註冊為自動化帳戶的 DSC 節點。</span><span class="sxs-lookup"><span data-stu-id="9f91c-103">Registers an Azure virtual machine as a DSC node for an Automation account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9f91c-104">句法</span><span class="sxs-lookup"><span data-stu-id="9f91c-104">SYNTAX</span></span>

```
Register-AzureRmAutomationDscNode -AzureVMName <String> [-NodeConfigurationName <String>]
 [-ConfigurationMode <String>] [-ConfigurationModeFrequencyMins <Int32>] [-RefreshFrequencyMins <Int32>]
 [-RebootNodeIfNeeded <Boolean>] [-ActionAfterReboot <String>] [-AllowModuleOverwrite <Boolean>]
 [-AzureVMResourceGroup <String>] [-AzureVMLocation <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f91c-105">說明</span><span class="sxs-lookup"><span data-stu-id="9f91c-105">DESCRIPTION</span></span>
<span data-ttu-id="9f91c-106">**AzureRmAutomationDscNode** Cmdlet 會在 azure 自動化帳戶中，將 Azure 虛擬機器註冊為所需的 Ap 狀態配置 (DSC) 節點。</span><span class="sxs-lookup"><span data-stu-id="9f91c-106">The **Register-AzureRmAutomationDscNode** cmdlet registers an Azure virtual machine as an APS Desired State Configuration (DSC) node in an Azure Automation account.</span></span>

## <span data-ttu-id="9f91c-107">示例</span><span class="sxs-lookup"><span data-stu-id="9f91c-107">EXAMPLES</span></span>

### <span data-ttu-id="9f91c-108">範例1：將 Azure 虛擬機器註冊為 Azure DSC 節點</span><span class="sxs-lookup"><span data-stu-id="9f91c-108">Example 1: Register an Azure virtual machine as an Azure DSC node</span></span>
```
PS C:\>Register-AzureRmAutomationDscNode -AutomationAccountName "Contoso17" -AzureVMName "VirtualMachine01" -ResourceGroupName "ResourceGroup01"-NodeConfigurationName "ContosoConfiguration.webserver"
```

<span data-ttu-id="9f91c-109">這個命令會將名為 VirtualMachine01 的 Azure 虛擬機器註冊為名為 Contoso17 的自動化帳戶中的 DSC 節點。</span><span class="sxs-lookup"><span data-stu-id="9f91c-109">This command registers the Azure virtual machine named VirtualMachine01 as a DSC node in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="9f91c-110">參數</span><span class="sxs-lookup"><span data-stu-id="9f91c-110">PARAMETERS</span></span>

### <span data-ttu-id="9f91c-111">-ActionAfterReboot</span><span class="sxs-lookup"><span data-stu-id="9f91c-111">-ActionAfterReboot</span></span>
<span data-ttu-id="9f91c-112">指定虛擬機器重新開機後所採取的動作。</span><span class="sxs-lookup"><span data-stu-id="9f91c-112">Specifies the action that the virtual machine takes after it restarts.</span></span>
<span data-ttu-id="9f91c-113">有效值為：</span><span class="sxs-lookup"><span data-stu-id="9f91c-113">Valid values are:</span></span> 

- <span data-ttu-id="9f91c-114">ContinueConfiguration</span><span class="sxs-lookup"><span data-stu-id="9f91c-114">ContinueConfiguration</span></span> 
- <span data-ttu-id="9f91c-115">StopConfiguration</span><span class="sxs-lookup"><span data-stu-id="9f91c-115">StopConfiguration</span></span>

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

### <span data-ttu-id="9f91c-116">-AllowModuleOverwrite</span><span class="sxs-lookup"><span data-stu-id="9f91c-116">-AllowModuleOverwrite</span></span>
<span data-ttu-id="9f91c-117">指定此 DSC 節點從 Azure 自動化 DSC pull 伺服器下載的新設定是否會取代已在目標節點上的現有模組。</span><span class="sxs-lookup"><span data-stu-id="9f91c-117">Specifies whether new configurations that this DSC node downloads from the Azure Automation DSC pull server replace the existing modules already on the target node.</span></span>

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

### <span data-ttu-id="9f91c-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9f91c-118">-AutomationAccountName</span></span>
<span data-ttu-id="9f91c-119">指定此 Cmdlet 註冊虛擬機器之自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="9f91c-119">Specifies the name of an Automation account in which this cmdlet registers a virtual machine.</span></span>

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

### <span data-ttu-id="9f91c-120">-AzureVMLocation</span><span class="sxs-lookup"><span data-stu-id="9f91c-120">-AzureVMLocation</span></span>
<span data-ttu-id="9f91c-121">指定此 Cmdlet 註冊虛擬機器的位置。</span><span class="sxs-lookup"><span data-stu-id="9f91c-121">Specifies the location in which this cmdlet registers a virtual machine.</span></span>
<span data-ttu-id="9f91c-122">若要取得有效的位置，請使用 Get-AzureRMLocation Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9f91c-122">To obtain valid locations, use the Get-AzureRMLocation cmdlet.</span></span>

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

### <span data-ttu-id="9f91c-123">-AzureVMName</span><span class="sxs-lookup"><span data-stu-id="9f91c-123">-AzureVMName</span></span>
<span data-ttu-id="9f91c-124">指定此 Cmdlet 註冊管理的 Azure 虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="9f91c-124">Specifies the name of the Azure virtual machine that this cmdlet registers for management.</span></span>

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

### <span data-ttu-id="9f91c-125">-AzureVMResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9f91c-125">-AzureVMResourceGroup</span></span>
<span data-ttu-id="9f91c-126">指定此 Cmdlet 註冊之 Azure 虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9f91c-126">Specifies the name of the resource group of the Azure virtual machine that this cmdlet registers.</span></span>

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

### <span data-ttu-id="9f91c-127">-ConfigurationMode</span><span class="sxs-lookup"><span data-stu-id="9f91c-127">-ConfigurationMode</span></span>
<span data-ttu-id="9f91c-128">指定 DSC 配置模式。</span><span class="sxs-lookup"><span data-stu-id="9f91c-128">Specifies the DSC configuration mode.</span></span>
<span data-ttu-id="9f91c-129">有效值為：</span><span class="sxs-lookup"><span data-stu-id="9f91c-129">Valid values are:</span></span> 

- <span data-ttu-id="9f91c-130">ApplyAndMonitor</span><span class="sxs-lookup"><span data-stu-id="9f91c-130">ApplyAndMonitor</span></span> 
- <span data-ttu-id="9f91c-131">ApplyAndAutocorrect</span><span class="sxs-lookup"><span data-stu-id="9f91c-131">ApplyAndAutocorrect</span></span> 
- <span data-ttu-id="9f91c-132">ApplyOnly</span><span class="sxs-lookup"><span data-stu-id="9f91c-132">ApplyOnly</span></span>

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

### <span data-ttu-id="9f91c-133">-ConfigurationModeFrequencyMins</span><span class="sxs-lookup"><span data-stu-id="9f91c-133">-ConfigurationModeFrequencyMins</span></span>
<span data-ttu-id="9f91c-134">指定 DSC 的背景應用程式嘗試在目標節點上實現目前設定的頻率（以分鐘為單位）。</span><span class="sxs-lookup"><span data-stu-id="9f91c-134">Specifies the frequency, in minutes, at which the background application of DSC attempts to implement the current configuration on the target node.</span></span>

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

### <span data-ttu-id="9f91c-135">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="9f91c-135">-NodeConfigurationName</span></span>
<span data-ttu-id="9f91c-136">指定此 Cmdlet 設定要從 Azure Automation DSC 納入的虛擬機器的節點配置名稱。</span><span class="sxs-lookup"><span data-stu-id="9f91c-136">Specifies the name of the node configuration that this cmdlet configures the virtual machine to pull from Azure Automation DSC.</span></span>

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

### <span data-ttu-id="9f91c-137">-RebootNodeIfNeeded</span><span class="sxs-lookup"><span data-stu-id="9f91c-137">-RebootNodeIfNeeded</span></span>
<span data-ttu-id="9f91c-138">指定是否要視需要重新開機虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="9f91c-138">Specifies whether to restart the virtual machine, if needed.</span></span>

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

### <span data-ttu-id="9f91c-139">-RefreshFrequencyMins</span><span class="sxs-lookup"><span data-stu-id="9f91c-139">-RefreshFrequencyMins</span></span>
<span data-ttu-id="9f91c-140">指定「本機 Configuration Manager」聯絡 Azure 自動化 DSC 拉伺服器以下載最新節點設定的頻率（以分鐘為單位）。</span><span class="sxs-lookup"><span data-stu-id="9f91c-140">Specifies the frequency, in minutes, at which the local Configuration Manager contacts the Azure Automation DSC pull server to download the latest node configuration.</span></span>

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

### <span data-ttu-id="9f91c-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f91c-141">-ResourceGroupName</span></span>
<span data-ttu-id="9f91c-142">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9f91c-142">Specifies the name of a resource group.</span></span>
<span data-ttu-id="9f91c-143">此 Cmdlet 註冊虛擬機器的自動化帳戶屬於此參數指定的資源群組。</span><span class="sxs-lookup"><span data-stu-id="9f91c-143">The Automation account with which this cmdlet registers a virtual machine belongs to the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="9f91c-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f91c-144">-DefaultProfile</span></span>
<span data-ttu-id="9f91c-145">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9f91c-145">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9f91c-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f91c-146">CommonParameters</span></span>
<span data-ttu-id="9f91c-147">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9f91c-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f91c-148">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9f91c-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f91c-149">輸入</span><span class="sxs-lookup"><span data-stu-id="9f91c-149">INPUTS</span></span>

## <span data-ttu-id="9f91c-150">輸出</span><span class="sxs-lookup"><span data-stu-id="9f91c-150">OUTPUTS</span></span>

## <span data-ttu-id="9f91c-151">筆記</span><span class="sxs-lookup"><span data-stu-id="9f91c-151">NOTES</span></span>

## <span data-ttu-id="9f91c-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="9f91c-152">RELATED LINKS</span></span>

[<span data-ttu-id="9f91c-153">AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="9f91c-153">Get-AzureRmAutomationDscNode</span></span>](./Get-AzureRmAutomationDscNode.md)

[<span data-ttu-id="9f91c-154">Set-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="9f91c-154">Set-AzureRmAutomationDscNode</span></span>](./Set-AzureRmAutomationDscNode.md)

[<span data-ttu-id="9f91c-155">取消註冊-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="9f91c-155">Unregister-AzureRmAutomationDscNode</span></span>](./Unregister-AzureRmAutomationDscNode.md)


