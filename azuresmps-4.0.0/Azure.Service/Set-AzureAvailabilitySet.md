---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: E0590AD4-F67B-48EF-8657-8890A2204CB6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 607cd288bcc9c86209a3ae0af569e964205f5cb4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967513"
---
# <span data-ttu-id="03527-101">Set-AzureAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="03527-101">Set-AzureAvailabilitySet</span></span>

## <span data-ttu-id="03527-102">摘要</span><span class="sxs-lookup"><span data-stu-id="03527-102">SYNOPSIS</span></span>
<span data-ttu-id="03527-103">在 Azure 虛擬機器上設定可用性集的名稱。</span><span class="sxs-lookup"><span data-stu-id="03527-103">Sets the name of the availability set on an Azure virtual machine.</span></span>

## <span data-ttu-id="03527-104">句法</span><span class="sxs-lookup"><span data-stu-id="03527-104">SYNTAX</span></span>

```
Set-AzureAvailabilitySet [-AvailabilitySetName] <String> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="03527-105">說明</span><span class="sxs-lookup"><span data-stu-id="03527-105">DESCRIPTION</span></span>
<span data-ttu-id="03527-106">**AzureAvailabilitySet** Cmdlet 會在部署後設定 Azure 虛擬機器上的可用性集名稱。</span><span class="sxs-lookup"><span data-stu-id="03527-106">The **Set-AzureAvailabilitySet** cmdlet sets the name of the availability set on an Azure virtual machine after deployment.</span></span>

## <span data-ttu-id="03527-107">示例</span><span class="sxs-lookup"><span data-stu-id="03527-107">EXAMPLES</span></span>

### <span data-ttu-id="03527-108">範例1：修改可用性集的名稱</span><span class="sxs-lookup"><span data-stu-id="03527-108">Example 1: Modify the name of an availability set</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine24" | Set-AzureAvailabilitySet -AvailabilitySetName "AvailabilitySet14" | Update-AzureVM
```

<span data-ttu-id="03527-109">第一個命令會透過使用 **xxxxx Cmdlet，** 在名為 ContosoService 的服務中，取得名為 VirtualMachine07 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="03527-109">The first command gets the virtual machine named VirtualMachine07 in the service named ContosoService by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="03527-110">命令會使用管線運算子，將該物件傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="03527-110">The command passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="03527-111">該 Cmdlet 會修改該虛擬機器的可用性集名稱。</span><span class="sxs-lookup"><span data-stu-id="03527-111">That cmdlet modifies the name of the availability set for that virtual machine.</span></span>
<span data-ttu-id="03527-112">此命令會更新虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="03527-112">The command updates the virtual machine.</span></span>

## <span data-ttu-id="03527-113">參數</span><span class="sxs-lookup"><span data-stu-id="03527-113">PARAMETERS</span></span>

### <span data-ttu-id="03527-114">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="03527-114">-AvailabilitySetName</span></span>
<span data-ttu-id="03527-115">指定虛擬機器所屬之可用性集的名稱。</span><span class="sxs-lookup"><span data-stu-id="03527-115">Specifies the name of the availability set to which the virtual machine belongs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03527-116">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="03527-116">-InformationAction</span></span>
<span data-ttu-id="03527-117">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="03527-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="03527-118">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="03527-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="03527-119">持續</span><span class="sxs-lookup"><span data-stu-id="03527-119">Continue</span></span>
- <span data-ttu-id="03527-120">理會</span><span class="sxs-lookup"><span data-stu-id="03527-120">Ignore</span></span>
- <span data-ttu-id="03527-121">看</span><span class="sxs-lookup"><span data-stu-id="03527-121">Inquire</span></span>
- <span data-ttu-id="03527-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="03527-122">SilentlyContinue</span></span>
- <span data-ttu-id="03527-123">停止</span><span class="sxs-lookup"><span data-stu-id="03527-123">Stop</span></span>
- <span data-ttu-id="03527-124">封存</span><span class="sxs-lookup"><span data-stu-id="03527-124">Suspend</span></span>

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

### <span data-ttu-id="03527-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="03527-125">-InformationVariable</span></span>
<span data-ttu-id="03527-126">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="03527-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="03527-127">-設定檔</span><span class="sxs-lookup"><span data-stu-id="03527-127">-Profile</span></span>
<span data-ttu-id="03527-128">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="03527-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="03527-129">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="03527-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="03527-130">-VM</span><span class="sxs-lookup"><span data-stu-id="03527-130">-VM</span></span>
<span data-ttu-id="03527-131">指定此 Cmdlet 修改的虛擬機器配置。</span><span class="sxs-lookup"><span data-stu-id="03527-131">Specifies the virtual machine configuration that this cmdlet modifies.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="03527-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03527-132">CommonParameters</span></span>
<span data-ttu-id="03527-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="03527-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03527-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="03527-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03527-135">輸入</span><span class="sxs-lookup"><span data-stu-id="03527-135">INPUTS</span></span>

## <span data-ttu-id="03527-136">輸出</span><span class="sxs-lookup"><span data-stu-id="03527-136">OUTPUTS</span></span>

## <span data-ttu-id="03527-137">筆記</span><span class="sxs-lookup"><span data-stu-id="03527-137">NOTES</span></span>

## <span data-ttu-id="03527-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="03527-138">RELATED LINKS</span></span>

[<span data-ttu-id="03527-139">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="03527-139">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="03527-140">移除-AzureAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="03527-140">Remove-AzureAvailabilitySet</span></span>](./Remove-AzureAvailabilitySet.md)


