---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: BBA0D5D3-29A5-4E00-9075-702E2F81CA52
online version: ''
schema: 2.0.0
ms.openlocfilehash: bcff7873042d9f7a07eee26f93312c8690e16416
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967993"
---
# <span data-ttu-id="f3c40-101">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="f3c40-101">Get-AzureVM</span></span>

## <span data-ttu-id="f3c40-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f3c40-102">SYNOPSIS</span></span>
<span data-ttu-id="f3c40-103">從一或多個 Azure 虛擬機器中檢索資訊。</span><span class="sxs-lookup"><span data-stu-id="f3c40-103">Retrieves information from one or more Azure virtual machines.</span></span>

## <span data-ttu-id="f3c40-104">句法</span><span class="sxs-lookup"><span data-stu-id="f3c40-104">SYNTAX</span></span>

### <span data-ttu-id="f3c40-105">ListAllVMs (預設) </span><span class="sxs-lookup"><span data-stu-id="f3c40-105">ListAllVMs (Default)</span></span>
```
Get-AzureVM [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="f3c40-106">GetVMByServiceAndVMName</span><span class="sxs-lookup"><span data-stu-id="f3c40-106">GetVMByServiceAndVMName</span></span>
```
Get-AzureVM [-ServiceName] <String> [[-Name] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="f3c40-107">說明</span><span class="sxs-lookup"><span data-stu-id="f3c40-107">DESCRIPTION</span></span>
<span data-ttu-id="f3c40-108">**Add-azurevm** Cmdlet 會檢索在 Azure 中執行之虛擬機器的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f3c40-108">The **Get-AzureVM** cmdlet retrieves information about virtual machines running in Azure.</span></span>
<span data-ttu-id="f3c40-109">它會傳回包含特定虛擬機器上資訊的物件，或者如果沒有指定虛擬機器，則會針對目前訂閱的指定服務中的所有虛擬機器傳回該物件。</span><span class="sxs-lookup"><span data-stu-id="f3c40-109">It returns an object with information on a specific virtual machine, or if no virtual machine is specified, for all the virtual machines in the specified service of the current subscription.</span></span>

## <span data-ttu-id="f3c40-110">示例</span><span class="sxs-lookup"><span data-stu-id="f3c40-110">EXAMPLES</span></span>

### <span data-ttu-id="f3c40-111">範例1：在指定的虛擬機器上檢索資訊</span><span class="sxs-lookup"><span data-stu-id="f3c40-111">Example 1: Retrieve information on a specified virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService01" -Name "VirtualMachine02"
```

<span data-ttu-id="f3c40-112">這個命令會傳回一個物件，其中包含在 ContosoService01 雲端服務中執行之 VirtualMachine02 虛擬機器的資訊。</span><span class="sxs-lookup"><span data-stu-id="f3c40-112">This command returns an object with information on the VirtualMachine02 virtual machine running in the ContosoService01 cloud service.</span></span>

### <span data-ttu-id="f3c40-113">範例2：在所有虛擬機器上檢索資訊</span><span class="sxs-lookup"><span data-stu-id="f3c40-113">Example 2: Retrieve information on all virtual machines</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService01"
```

<span data-ttu-id="f3c40-114">這個命令會以 ContosoService01 雲端服務中執行的所有虛擬機器資訊來檢索清單物件。</span><span class="sxs-lookup"><span data-stu-id="f3c40-114">This command retrieves a list object with information on all of the virtual machines running in the ContosoService01 cloud service.</span></span>

### <span data-ttu-id="f3c40-115">範例3：顯示虛擬機器狀態資料表</span><span class="sxs-lookup"><span data-stu-id="f3c40-115">Example 3: Display a table of virtual machine statuses</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService01"  | Format-Table AutoSize -Property "Name",@{Expression={$_.InstanceUpgradeDomain};Label="UpgDom";Align="Right"},"InstanceStatus"
```

<span data-ttu-id="f3c40-116">這個命令會顯示一個表格，其中顯示在 ContosoService01 服務上執行的虛擬機器、其升級網域，以及每個虛擬機器的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="f3c40-116">This command displays a table showing the virtual machines running on the ContosoService01 service, their Upgrade Domain, and the current status of each virtual machine.</span></span>

## <span data-ttu-id="f3c40-117">參數</span><span class="sxs-lookup"><span data-stu-id="f3c40-117">PARAMETERS</span></span>

### <span data-ttu-id="f3c40-118">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="f3c40-118">-InformationAction</span></span>
<span data-ttu-id="f3c40-119">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="f3c40-119">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="f3c40-120">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="f3c40-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f3c40-121">持續</span><span class="sxs-lookup"><span data-stu-id="f3c40-121">Continue</span></span>
- <span data-ttu-id="f3c40-122">理會</span><span class="sxs-lookup"><span data-stu-id="f3c40-122">Ignore</span></span>
- <span data-ttu-id="f3c40-123">看</span><span class="sxs-lookup"><span data-stu-id="f3c40-123">Inquire</span></span>
- <span data-ttu-id="f3c40-124">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="f3c40-124">SilentlyContinue</span></span>
- <span data-ttu-id="f3c40-125">停止</span><span class="sxs-lookup"><span data-stu-id="f3c40-125">Stop</span></span>
- <span data-ttu-id="f3c40-126">封存</span><span class="sxs-lookup"><span data-stu-id="f3c40-126">Suspend</span></span>

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

### <span data-ttu-id="f3c40-127">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="f3c40-127">-InformationVariable</span></span>
<span data-ttu-id="f3c40-128">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="f3c40-128">Specifies an information variable.</span></span>

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

### <span data-ttu-id="f3c40-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="f3c40-129">-Name</span></span>
<span data-ttu-id="f3c40-130">指定要為其檢索資訊之虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="f3c40-130">Specifies the name of the virtual machine for which to retrieve information.</span></span>
<span data-ttu-id="f3c40-131">如果未提供此參數，則 Cmdlet 會傳回清單物件，其中包含有關指定服務中所有虛擬機器的資訊。</span><span class="sxs-lookup"><span data-stu-id="f3c40-131">If this parameter is not provided, the cmdlet returns a list object with information about all the virtual machines in the specified service.</span></span>

```yaml
Type: String
Parameter Sets: GetVMByServiceAndVMName
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3c40-132">-設定檔</span><span class="sxs-lookup"><span data-stu-id="f3c40-132">-Profile</span></span>
<span data-ttu-id="f3c40-133">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="f3c40-133">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f3c40-134">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="f3c40-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f3c40-135">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="f3c40-135">-ServiceName</span></span>
<span data-ttu-id="f3c40-136">指定要傳回虛擬機器資訊之雲端服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="f3c40-136">Specifies the name of the cloud service for which to return virtual machine information.</span></span>

```yaml
Type: String
Parameter Sets: GetVMByServiceAndVMName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3c40-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3c40-137">CommonParameters</span></span>
<span data-ttu-id="f3c40-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f3c40-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3c40-139">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f3c40-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3c40-140">輸入</span><span class="sxs-lookup"><span data-stu-id="f3c40-140">INPUTS</span></span>

## <span data-ttu-id="f3c40-141">輸出</span><span class="sxs-lookup"><span data-stu-id="f3c40-141">OUTPUTS</span></span>

## <span data-ttu-id="f3c40-142">筆記</span><span class="sxs-lookup"><span data-stu-id="f3c40-142">NOTES</span></span>

## <span data-ttu-id="f3c40-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="f3c40-143">RELATED LINKS</span></span>

[<span data-ttu-id="f3c40-144">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="f3c40-144">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="f3c40-145">新-AzureVMConfig</span><span class="sxs-lookup"><span data-stu-id="f3c40-145">New-AzureVMConfig</span></span>](./New-AzureVMConfig.md)

[<span data-ttu-id="f3c40-146">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="f3c40-146">Remove-AzureVM</span></span>](./Remove-AzureVM.md)

[<span data-ttu-id="f3c40-147">Restart-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="f3c40-147">Restart-AzureVM</span></span>](./Restart-AzureVM.md)

[<span data-ttu-id="f3c40-148">開始-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="f3c40-148">Start-AzureVM</span></span>](./Start-AzureVM.md)

[<span data-ttu-id="f3c40-149">靜幀</span><span class="sxs-lookup"><span data-stu-id="f3c40-149">Stop-AzureVM</span></span>](./Stop-AzureVM.md)

[<span data-ttu-id="f3c40-150">更新-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="f3c40-150">Update-AzureVM</span></span>](./Update-AzureVM.md)


