---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 4F347DD1-907C-47DB-8F1D-636DE031A56A
online version: ''
schema: 2.0.0
ms.openlocfilehash: e01265cf3db8a0dc3fd9d74a4a263a20965b10fb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967187"
---
# <span data-ttu-id="53453-101">Stop-AzureVM</span><span class="sxs-lookup"><span data-stu-id="53453-101">Stop-AzureVM</span></span>

## <span data-ttu-id="53453-102">摘要</span><span class="sxs-lookup"><span data-stu-id="53453-102">SYNOPSIS</span></span>
<span data-ttu-id="53453-103">關閉 Azure 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="53453-103">Shuts down an Azure virtual machine.</span></span>

## <span data-ttu-id="53453-104">句法</span><span class="sxs-lookup"><span data-stu-id="53453-104">SYNTAX</span></span>

### <span data-ttu-id="53453-105">ByName (預設) </span><span class="sxs-lookup"><span data-stu-id="53453-105">ByName (Default)</span></span>
```
Stop-AzureVM [-Name] <String[]> [-StayProvisioned] [-Force] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="53453-106">輸出</span><span class="sxs-lookup"><span data-stu-id="53453-106">Input</span></span>
```
Stop-AzureVM -VM <IPersistentVM[]> [-StayProvisioned] [-Force] [-ServiceName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="53453-107">說明</span><span class="sxs-lookup"><span data-stu-id="53453-107">DESCRIPTION</span></span>
<span data-ttu-id="53453-108">**Stop-add-azurevm** Cmdlet 會關閉虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="53453-108">The **Stop-AzureVM** cmdlet shuts down a virtual machine.</span></span>

## <span data-ttu-id="53453-109">示例</span><span class="sxs-lookup"><span data-stu-id="53453-109">EXAMPLES</span></span>

### <span data-ttu-id="53453-110">範例1：關閉虛擬機器</span><span class="sxs-lookup"><span data-stu-id="53453-110">Example 1: Shut down a virtual machine</span></span>
```
PS C:\> Stop-AzureVM -ServiceName "ContosoService01" -Name "MyVM"
```

<span data-ttu-id="53453-111">這個命令會關閉指定服務所包含的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="53453-111">This command shuts down a virtual machine that the specified service contains.</span></span>

### <span data-ttu-id="53453-112">範例2：使用虛擬電腦物件關閉虛擬機器</span><span class="sxs-lookup"><span data-stu-id="53453-112">Example 2: Shut down a virtual machine by using a virtual machine object</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService01" -Name "MyVM" | Stop-AzureVM
```

<span data-ttu-id="53453-113">這個命令會透過使用由 **add-azurevm** 傳回的虛擬機器物件，來關閉指定服務所包含的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="53453-113">This command shuts down a virtual machine that the specified service contains, by using the virtual machine object that **Get-AzureVM** returns.</span></span>

### <span data-ttu-id="53453-114">範例3：關閉 VM 並保持 VM 已預配</span><span class="sxs-lookup"><span data-stu-id="53453-114">Example 3: Shut down a VM and keep the VM provisioned</span></span>
```
PS C:\> Stop-AzureVM -ServiceName "ContosoService01" -Name "MyVM" -StayProvisioned
```

<span data-ttu-id="53453-115">這個命令會關閉指定服務所包含的虛擬機器，並保持其已預配。</span><span class="sxs-lookup"><span data-stu-id="53453-115">This command shuts down a virtual machine that the specified service contains, and keeps it provisioned.</span></span>

### <span data-ttu-id="53453-116">範例4：關閉 VM 並允許解除在部署中的最後一個 VM</span><span class="sxs-lookup"><span data-stu-id="53453-116">Example 4: Shut down a VM and allow deallocation of the last VM in the deployment</span></span>
```
PS C:\> Stop-AzureVM -ServiceName "ContosoService01" -Name "MyVM" -Force
```

<span data-ttu-id="53453-117">這個命令會關閉指定服務所包含的虛擬機器，並允許解除部署中的最後一個虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="53453-117">This command shuts down a virtual machine that the specified service contains and allows deallocation of the last virtual machine in the deployment.</span></span>

### <span data-ttu-id="53453-118">範例5：關閉多個 Vm</span><span class="sxs-lookup"><span data-stu-id="53453-118">Example 5: Shut down multiple VMs</span></span>
```
PS C:\> Stop-AzureVM -ServiceName "PSTestService" -Name "*" -Force
```

<span data-ttu-id="53453-119">這個命令會關閉指定服務所包含的多個虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="53453-119">This command shuts down multiple virtual machines that the specified service contains.</span></span>

## <span data-ttu-id="53453-120">參數</span><span class="sxs-lookup"><span data-stu-id="53453-120">PARAMETERS</span></span>

### <span data-ttu-id="53453-121">-Force</span><span class="sxs-lookup"><span data-stu-id="53453-121">-Force</span></span>
<span data-ttu-id="53453-122">指定是否允許解除配置部署中的最後一個虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="53453-122">Specifies whether to allow the deallocation of the last virtual machine in a deployment.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53453-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="53453-123">-InformationAction</span></span>
<span data-ttu-id="53453-124">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="53453-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="53453-125">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="53453-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="53453-126">持續</span><span class="sxs-lookup"><span data-stu-id="53453-126">Continue</span></span>
- <span data-ttu-id="53453-127">理會</span><span class="sxs-lookup"><span data-stu-id="53453-127">Ignore</span></span>
- <span data-ttu-id="53453-128">看</span><span class="sxs-lookup"><span data-stu-id="53453-128">Inquire</span></span>
- <span data-ttu-id="53453-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="53453-129">SilentlyContinue</span></span>
- <span data-ttu-id="53453-130">停止</span><span class="sxs-lookup"><span data-stu-id="53453-130">Stop</span></span>
- <span data-ttu-id="53453-131">封存</span><span class="sxs-lookup"><span data-stu-id="53453-131">Suspend</span></span>

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

### <span data-ttu-id="53453-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="53453-132">-InformationVariable</span></span>
<span data-ttu-id="53453-133">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="53453-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="53453-134">-名稱</span><span class="sxs-lookup"><span data-stu-id="53453-134">-Name</span></span>
<span data-ttu-id="53453-135">指定要關閉的虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="53453-135">Specifies the name of the virtual machine to shut down.</span></span>

<span data-ttu-id="53453-136">使用萬用字元來非同步停止多個虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="53453-136">Use the wildcard character to stop multiple virtual machines asynchronously.</span></span>
<span data-ttu-id="53453-137">使用萬用字元時，這個 Cmdlet 會呼叫關閉角色作業 https://msdn.microsoft.com/en-us/library/azure/dn469421.aspx (https://msdn.microsoft.com/en-us/library/azure/dn469421.aspx) ，而不是關閉角色 https://msdn.microsoft.com/en-us/library/azure/jj157195.aspx 操作 (https://msdn.microsoft.com/en-us/library/azure/jj157195.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="53453-137">With a wildcard character, this cmdlet calls the Shutdown Roleshttps://msdn.microsoft.com/en-us/library/azure/dn469421.aspx operation (https://msdn.microsoft.com/en-us/library/azure/dn469421.aspx), instead of the Shutdown Rolehttps://msdn.microsoft.com/en-us/library/azure/jj157195.aspx operation (https://msdn.microsoft.com/en-us/library/azure/jj157195.aspx).</span></span>

```yaml
Type: String[]
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53453-138">-設定檔</span><span class="sxs-lookup"><span data-stu-id="53453-138">-Profile</span></span>
<span data-ttu-id="53453-139">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="53453-139">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="53453-140">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="53453-140">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="53453-141">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="53453-141">-ServiceName</span></span>
<span data-ttu-id="53453-142">指定包含要關閉之虛擬機器之 Azure 服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="53453-142">Specifies the name of the Azure service that contains the virtual machine to shut down.</span></span>

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

### <span data-ttu-id="53453-143">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="53453-143">-StayProvisioned</span></span>
<span data-ttu-id="53453-144">指定此 Cmdlet 會保留預配的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="53453-144">Specifies that this cmdlet keeps the virtual machine provisioned.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53453-145">-VM</span><span class="sxs-lookup"><span data-stu-id="53453-145">-VM</span></span>
<span data-ttu-id="53453-146">指定識別要關閉之虛擬機器的虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="53453-146">Specifies a virtual machine object that identifies the virtual machine to shut down.</span></span>

```yaml
Type: IPersistentVM[]
Parameter Sets: Input
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53453-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53453-147">CommonParameters</span></span>
<span data-ttu-id="53453-148">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="53453-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53453-149">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="53453-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53453-150">輸入</span><span class="sxs-lookup"><span data-stu-id="53453-150">INPUTS</span></span>

## <span data-ttu-id="53453-151">輸出</span><span class="sxs-lookup"><span data-stu-id="53453-151">OUTPUTS</span></span>

## <span data-ttu-id="53453-152">筆記</span><span class="sxs-lookup"><span data-stu-id="53453-152">NOTES</span></span>

## <span data-ttu-id="53453-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="53453-153">RELATED LINKS</span></span>

[<span data-ttu-id="53453-154">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="53453-154">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="53453-155">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="53453-155">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="53453-156">Restart-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="53453-156">Restart-AzureVM</span></span>](./Restart-AzureVM.md)

[<span data-ttu-id="53453-157">開始-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="53453-157">Start-AzureVM</span></span>](./Start-AzureVM.md)


