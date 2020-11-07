---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 73CEA6A8-46C9-4772-9A67-03F532696CFD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6c1287b3a0bb1cc39dea78fb4e92d2dcc4508c6a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93966989"
---
# <span data-ttu-id="563fd-101">Get-AzureSubnet</span><span class="sxs-lookup"><span data-stu-id="563fd-101">Get-AzureSubnet</span></span>

## <span data-ttu-id="563fd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="563fd-102">SYNOPSIS</span></span>
<span data-ttu-id="563fd-103">取得與指定的 Azure 虛擬機器相關聯之子網的清單。</span><span class="sxs-lookup"><span data-stu-id="563fd-103">Gets a list of subnets associated with the specified Azure virtual machine.</span></span>

## <span data-ttu-id="563fd-104">句法</span><span class="sxs-lookup"><span data-stu-id="563fd-104">SYNTAX</span></span>

```
Get-AzureSubnet -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="563fd-105">說明</span><span class="sxs-lookup"><span data-stu-id="563fd-105">DESCRIPTION</span></span>
<span data-ttu-id="563fd-106">**AzureSubnet** Cmdlet 會傳回與指定的虛擬機器相關聯之子網的清單。</span><span class="sxs-lookup"><span data-stu-id="563fd-106">The **Get-AzureSubnet** cmdlet returns a list the subnets associated with the specified virtual machine.</span></span>
<span data-ttu-id="563fd-107">使用 **add-azurevm** 來指定虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="563fd-107">Use **Get-AzureVM** to specify the virtual machine.</span></span>

## <span data-ttu-id="563fd-108">示例</span><span class="sxs-lookup"><span data-stu-id="563fd-108">EXAMPLES</span></span>

### <span data-ttu-id="563fd-109">範例1：取得虛擬機器的子網</span><span class="sxs-lookup"><span data-stu-id="563fd-109">Example 1: Get subnets for a virtual machine</span></span>
```
PS C:\> $VM = Get-AzureVM -ServiceName "ContosoService03" -Name "VirtualMachine01"
C:\PS> Get-AzureSubnet -VM $VM
```

<span data-ttu-id="563fd-110">第一個命令會在名為 ContosoService03 的服務中，取得一個名為 VirtualMachine01 的虛擬機器，然後將它儲存在 $VM 變數中。</span><span class="sxs-lookup"><span data-stu-id="563fd-110">The first command gets a virtual machine named VirtualMachine01 in the service named ContosoService03, and then stores it in the $VM variable.</span></span>

<span data-ttu-id="563fd-111">第二個命令會在 $VM 中取得虛擬機器的 Azure 子網。</span><span class="sxs-lookup"><span data-stu-id="563fd-111">The second command gets the Azure subnets for the virtual machine in $VM.</span></span>

## <span data-ttu-id="563fd-112">參數</span><span class="sxs-lookup"><span data-stu-id="563fd-112">PARAMETERS</span></span>

### <span data-ttu-id="563fd-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="563fd-113">-InformationAction</span></span>
<span data-ttu-id="563fd-114">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="563fd-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="563fd-115">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="563fd-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="563fd-116">持續</span><span class="sxs-lookup"><span data-stu-id="563fd-116">Continue</span></span>
- <span data-ttu-id="563fd-117">理會</span><span class="sxs-lookup"><span data-stu-id="563fd-117">Ignore</span></span>
- <span data-ttu-id="563fd-118">看</span><span class="sxs-lookup"><span data-stu-id="563fd-118">Inquire</span></span>
- <span data-ttu-id="563fd-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="563fd-119">SilentlyContinue</span></span>
- <span data-ttu-id="563fd-120">停止</span><span class="sxs-lookup"><span data-stu-id="563fd-120">Stop</span></span>
- <span data-ttu-id="563fd-121">封存</span><span class="sxs-lookup"><span data-stu-id="563fd-121">Suspend</span></span>

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

### <span data-ttu-id="563fd-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="563fd-122">-InformationVariable</span></span>
<span data-ttu-id="563fd-123">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="563fd-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="563fd-124">-設定檔</span><span class="sxs-lookup"><span data-stu-id="563fd-124">-Profile</span></span>
<span data-ttu-id="563fd-125">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="563fd-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="563fd-126">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="563fd-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="563fd-127">-VM</span><span class="sxs-lookup"><span data-stu-id="563fd-127">-VM</span></span>
<span data-ttu-id="563fd-128">指定要從中取得子網清單的虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="563fd-128">Specifies the virtual machine object from which to get the subnet list.</span></span>

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

### <span data-ttu-id="563fd-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="563fd-129">CommonParameters</span></span>
<span data-ttu-id="563fd-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="563fd-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="563fd-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="563fd-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="563fd-132">輸入</span><span class="sxs-lookup"><span data-stu-id="563fd-132">INPUTS</span></span>

## <span data-ttu-id="563fd-133">輸出</span><span class="sxs-lookup"><span data-stu-id="563fd-133">OUTPUTS</span></span>

## <span data-ttu-id="563fd-134">筆記</span><span class="sxs-lookup"><span data-stu-id="563fd-134">NOTES</span></span>

## <span data-ttu-id="563fd-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="563fd-135">RELATED LINKS</span></span>

[<span data-ttu-id="563fd-136">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="563fd-136">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="563fd-137">Set-AzureSubnet</span><span class="sxs-lookup"><span data-stu-id="563fd-137">Set-AzureSubnet</span></span>](./Set-AzureSubnet.md)


