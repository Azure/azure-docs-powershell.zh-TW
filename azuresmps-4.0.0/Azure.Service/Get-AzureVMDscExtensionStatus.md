---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 19A87B24-C5A6-4505-BB54-973B24BCC68E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 821927fc465ed5af048a2f27ed84da8c12b9caa5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967982"
---
# <span data-ttu-id="49360-101">Get-AzureVMDscExtensionStatus</span><span class="sxs-lookup"><span data-stu-id="49360-101">Get-AzureVMDscExtensionStatus</span></span>

## <span data-ttu-id="49360-102">摘要</span><span class="sxs-lookup"><span data-stu-id="49360-102">SYNOPSIS</span></span>
<span data-ttu-id="49360-103">取得雲端服務中部署之所有虛擬機器或服務中特定虛擬機器的 DSC 副檔名狀態。</span><span class="sxs-lookup"><span data-stu-id="49360-103">Gets the DSC extension status for all the virtual machines deployed in a cloud service or for a particular virtual machine in the service.</span></span>

## <span data-ttu-id="49360-104">句法</span><span class="sxs-lookup"><span data-stu-id="49360-104">SYNTAX</span></span>

### <span data-ttu-id="49360-105">GetStatusByServiceAndVMName (預設) </span><span class="sxs-lookup"><span data-stu-id="49360-105">GetStatusByServiceAndVMName (Default)</span></span>
```
Get-AzureVMDscExtensionStatus [-ServiceName] <String> [[-Name] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="49360-106">GetStatusByVM</span><span class="sxs-lookup"><span data-stu-id="49360-106">GetStatusByVM</span></span>
```
Get-AzureVMDscExtensionStatus -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="49360-107">說明</span><span class="sxs-lookup"><span data-stu-id="49360-107">DESCRIPTION</span></span>
<span data-ttu-id="49360-108">AzureVMDscExtensionStatus Cmdlet 會針對部署在雲端服務中的所有虛擬機器或服務中的特定虛擬機器， **取得** 所需的狀態設定 (DSC) 副檔名狀態。</span><span class="sxs-lookup"><span data-stu-id="49360-108">The **Get-AzureVMDscExtensionStatus** cmdlet gets the Desired State Configuration (DSC) extension status for all the virtual machines deployed in a cloud service or for a particular virtual machine in the service.</span></span>

## <span data-ttu-id="49360-109">示例</span><span class="sxs-lookup"><span data-stu-id="49360-109">EXAMPLES</span></span>

### <span data-ttu-id="49360-110">sr-1</span><span class="sxs-lookup"><span data-stu-id="49360-110">1:</span></span>
```

```

## <span data-ttu-id="49360-111">參數</span><span class="sxs-lookup"><span data-stu-id="49360-111">PARAMETERS</span></span>

### <span data-ttu-id="49360-112">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="49360-112">-InformationAction</span></span>
<span data-ttu-id="49360-113">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="49360-113">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="49360-114">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="49360-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="49360-115">持續</span><span class="sxs-lookup"><span data-stu-id="49360-115">Continue</span></span>
- <span data-ttu-id="49360-116">理會</span><span class="sxs-lookup"><span data-stu-id="49360-116">Ignore</span></span>
- <span data-ttu-id="49360-117">看</span><span class="sxs-lookup"><span data-stu-id="49360-117">Inquire</span></span>
- <span data-ttu-id="49360-118">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="49360-118">SilentlyContinue</span></span>
- <span data-ttu-id="49360-119">停止</span><span class="sxs-lookup"><span data-stu-id="49360-119">Stop</span></span>
- <span data-ttu-id="49360-120">封存</span><span class="sxs-lookup"><span data-stu-id="49360-120">Suspend</span></span>

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

### <span data-ttu-id="49360-121">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="49360-121">-InformationVariable</span></span>
<span data-ttu-id="49360-122">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="49360-122">Specifies an information variable.</span></span>

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

### <span data-ttu-id="49360-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="49360-123">-Name</span></span>
<span data-ttu-id="49360-124">指定虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="49360-124">Specifies the name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: GetStatusByServiceAndVMName
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49360-125">-設定檔</span><span class="sxs-lookup"><span data-stu-id="49360-125">-Profile</span></span>
<span data-ttu-id="49360-126">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="49360-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="49360-127">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="49360-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="49360-128">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="49360-128">-ServiceName</span></span>
<span data-ttu-id="49360-129">指定服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="49360-129">Specifies the name of the service.</span></span>

```yaml
Type: String
Parameter Sets: GetStatusByServiceAndVMName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49360-130">-VM</span><span class="sxs-lookup"><span data-stu-id="49360-130">-VM</span></span>
<span data-ttu-id="49360-131">指定持久性虛擬電腦物件。</span><span class="sxs-lookup"><span data-stu-id="49360-131">Specifies the persistent virtual machine object.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: GetStatusByVM
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="49360-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49360-132">CommonParameters</span></span>
<span data-ttu-id="49360-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="49360-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49360-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="49360-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49360-135">輸入</span><span class="sxs-lookup"><span data-stu-id="49360-135">INPUTS</span></span>

## <span data-ttu-id="49360-136">輸出</span><span class="sxs-lookup"><span data-stu-id="49360-136">OUTPUTS</span></span>

### <span data-ttu-id="49360-137">VirtualMachineDscExtensionStatusCoNtext WindowsAzure. ServiceManagement。</span><span class="sxs-lookup"><span data-stu-id="49360-137">Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.VirtualMachineDscExtensionStatusContext</span></span>

## <span data-ttu-id="49360-138">筆記</span><span class="sxs-lookup"><span data-stu-id="49360-138">NOTES</span></span>

## <span data-ttu-id="49360-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="49360-139">RELATED LINKS</span></span>

[<span data-ttu-id="49360-140">AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="49360-140">Get-AzureVMDscExtension</span></span>](./Get-AzureVMDscExtension.md)

[<span data-ttu-id="49360-141">移除-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="49360-141">Remove-AzureVMDscExtension</span></span>](./Remove-AzureVMDscExtension.md)

[<span data-ttu-id="49360-142">Set-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="49360-142">Set-AzureVMDscExtension</span></span>](./Set-AzureVMDscExtension.md)


