---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 596B8A6F-D3C2-4170-BCD7-B7A1CDB656D8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7ee767e1ba4c5008837e7cef98aafa4017465829
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967519"
---
# <span data-ttu-id="8315b-101">Restart-AzureVM</span><span class="sxs-lookup"><span data-stu-id="8315b-101">Restart-AzureVM</span></span>

## <span data-ttu-id="8315b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8315b-102">SYNOPSIS</span></span>
<span data-ttu-id="8315b-103">重新開機 Azure 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="8315b-103">Restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="8315b-104">句法</span><span class="sxs-lookup"><span data-stu-id="8315b-104">SYNTAX</span></span>

### <span data-ttu-id="8315b-105">RestartByName (預設) </span><span class="sxs-lookup"><span data-stu-id="8315b-105">RestartByName (Default)</span></span>
```
Restart-AzureVM [-Name] <String> [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="8315b-106">RedeployByName</span><span class="sxs-lookup"><span data-stu-id="8315b-106">RedeployByName</span></span>
```
Restart-AzureVM [-Name] <String> [-Redeploy] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="8315b-107">InitiateMaintenanceByName</span><span class="sxs-lookup"><span data-stu-id="8315b-107">InitiateMaintenanceByName</span></span>
```
Restart-AzureVM [-Name] <String> [-InitiateMaintenance] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="8315b-108">RestartInput</span><span class="sxs-lookup"><span data-stu-id="8315b-108">RestartInput</span></span>
```
Restart-AzureVM -VM <PersistentVM> [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="8315b-109">RedeployInput</span><span class="sxs-lookup"><span data-stu-id="8315b-109">RedeployInput</span></span>
```
Restart-AzureVM -VM <PersistentVM> [-Redeploy] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="8315b-110">InitiateMaintenanceInput</span><span class="sxs-lookup"><span data-stu-id="8315b-110">InitiateMaintenanceInput</span></span>
```
Restart-AzureVM -VM <PersistentVM> [-InitiateMaintenance] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="8315b-111">說明</span><span class="sxs-lookup"><span data-stu-id="8315b-111">DESCRIPTION</span></span>
<span data-ttu-id="8315b-112">**Restart （add-azurevm）** Cmdlet 會要求重新開機 Azure 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="8315b-112">The **Restart-AzureVM** cmdlet requests a restart of an Azure virtual machine.</span></span>

## <span data-ttu-id="8315b-113">示例</span><span class="sxs-lookup"><span data-stu-id="8315b-113">EXAMPLES</span></span>

### <span data-ttu-id="8315b-114">範例1：重新開機虛擬機器</span><span class="sxs-lookup"><span data-stu-id="8315b-114">Example 1: Restart a virtual machine</span></span>
```
PS C:\> Restart-AzureVM -ServiceName "MyService01" -Name "MyVM"
```

<span data-ttu-id="8315b-115">這個命令會重新開機在名為 Service01 的 Azure 服務中執行的 VirtualMachine27 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="8315b-115">This command restarts the VirtualMachine27 virtual machine running in the Azure service named Service01.</span></span>

### <span data-ttu-id="8315b-116">範例2：使用虛擬電腦物件重新開機虛擬機器</span><span class="sxs-lookup"><span data-stu-id="8315b-116">Example 2: Restart a virtual machine by using a virtual machine object</span></span>
```
PS C:\> Get-AzureVM -ServiceName "MyService01" -Name "VirtualMachine27" | Restart-AzureVM
```

<span data-ttu-id="8315b-117">這個命令會檢索名為 MyVM 的虛擬機器的虛擬機器物件，然後重新開機它。</span><span class="sxs-lookup"><span data-stu-id="8315b-117">This command retrieves the virtual machine object for the virtual machine named MyVM and then restarts it.</span></span>

## <span data-ttu-id="8315b-118">參數</span><span class="sxs-lookup"><span data-stu-id="8315b-118">PARAMETERS</span></span>

### <span data-ttu-id="8315b-119">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="8315b-119">-InformationAction</span></span>
<span data-ttu-id="8315b-120">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="8315b-120">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="8315b-121">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="8315b-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8315b-122">持續</span><span class="sxs-lookup"><span data-stu-id="8315b-122">Continue</span></span>
- <span data-ttu-id="8315b-123">理會</span><span class="sxs-lookup"><span data-stu-id="8315b-123">Ignore</span></span>
- <span data-ttu-id="8315b-124">看</span><span class="sxs-lookup"><span data-stu-id="8315b-124">Inquire</span></span>
- <span data-ttu-id="8315b-125">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="8315b-125">SilentlyContinue</span></span>
- <span data-ttu-id="8315b-126">停止</span><span class="sxs-lookup"><span data-stu-id="8315b-126">Stop</span></span>
- <span data-ttu-id="8315b-127">封存</span><span class="sxs-lookup"><span data-stu-id="8315b-127">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8315b-128">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="8315b-128">-InformationVariable</span></span>
<span data-ttu-id="8315b-129">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="8315b-129">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8315b-130">-InitiateMaintenance</span><span class="sxs-lookup"><span data-stu-id="8315b-130">-InitiateMaintenance</span></span>
<span data-ttu-id="8315b-131">在虛擬機器上啟動維護</span><span class="sxs-lookup"><span data-stu-id="8315b-131">Initiate Maintenance on the Virtual Machine</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: InitiateMaintenanceByName, InitiateMaintenanceInput
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8315b-132">-名稱</span><span class="sxs-lookup"><span data-stu-id="8315b-132">-Name</span></span>
<span data-ttu-id="8315b-133">指定要重新開機的虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="8315b-133">Specifies the name of the virtual machine to restart.</span></span>

```yaml
Type: String
Parameter Sets: RestartByName, RedeployByName, InitiateMaintenanceByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8315b-134">-設定檔</span><span class="sxs-lookup"><span data-stu-id="8315b-134">-Profile</span></span>
<span data-ttu-id="8315b-135">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="8315b-135">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8315b-136">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="8315b-136">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8315b-137">-重新部署</span><span class="sxs-lookup"><span data-stu-id="8315b-137">-Redeploy</span></span>
<span data-ttu-id="8315b-138">表示 redeploys 虛擬機器的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8315b-138">Indicates that the cmdlet redeploys the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RedeployByName, RedeployInput
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8315b-139">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="8315b-139">-ServiceName</span></span>
<span data-ttu-id="8315b-140">指定包含要重新開機之虛擬機器之 Azure 服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="8315b-140">Specifies the name of the Azure service that contains the virtual machine to restart.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8315b-141">-VM</span><span class="sxs-lookup"><span data-stu-id="8315b-141">-VM</span></span>
<span data-ttu-id="8315b-142">指定識別要重新開機之虛擬機器的虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="8315b-142">Specifies a virtual machine object that identifies the virtual machine to restart.</span></span>

```yaml
Type: PersistentVM
Parameter Sets: RestartInput, RedeployInput, InitiateMaintenanceInput
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8315b-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8315b-143">CommonParameters</span></span>
<span data-ttu-id="8315b-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8315b-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8315b-145">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8315b-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8315b-146">輸入</span><span class="sxs-lookup"><span data-stu-id="8315b-146">INPUTS</span></span>

## <span data-ttu-id="8315b-147">輸出</span><span class="sxs-lookup"><span data-stu-id="8315b-147">OUTPUTS</span></span>

## <span data-ttu-id="8315b-148">筆記</span><span class="sxs-lookup"><span data-stu-id="8315b-148">NOTES</span></span>

## <span data-ttu-id="8315b-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="8315b-149">RELATED LINKS</span></span>

[<span data-ttu-id="8315b-150">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="8315b-150">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="8315b-151">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="8315b-151">Remove-AzureVM</span></span>](./Remove-AzureVM.md)

[<span data-ttu-id="8315b-152">開始-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="8315b-152">Start-AzureVM</span></span>](./Start-AzureVM.md)

[<span data-ttu-id="8315b-153">靜幀</span><span class="sxs-lookup"><span data-stu-id="8315b-153">Stop-AzureVM</span></span>](./Stop-AzureVM.md)

[<span data-ttu-id="8315b-154">更新-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="8315b-154">Update-AzureVM</span></span>](./Update-AzureVM.md)


