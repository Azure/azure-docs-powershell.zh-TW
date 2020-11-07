---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 1721107D-22FF-4A42-93C6-FD812DF81C33
online version: ''
schema: 2.0.0
ms.openlocfilehash: ac1bb63645b8db9e6a66971ad4ecd3b545a39100
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967991"
---
# <span data-ttu-id="8c850-101">Get-AzureVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="8c850-101">Get-AzureVMChefExtension</span></span>

## <span data-ttu-id="8c850-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8c850-102">SYNOPSIS</span></span>
<span data-ttu-id="8c850-103">取得在虛擬機器上套用的主廚延伸。</span><span class="sxs-lookup"><span data-stu-id="8c850-103">Gets the Chef extension applied on a virtual machine.</span></span>

## <span data-ttu-id="8c850-104">句法</span><span class="sxs-lookup"><span data-stu-id="8c850-104">SYNTAX</span></span>

```
Get-AzureVMChefExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="8c850-105">說明</span><span class="sxs-lookup"><span data-stu-id="8c850-105">DESCRIPTION</span></span>
<span data-ttu-id="8c850-106">**AzureVMChefExtension** Cmdlet 會取得在虛擬機器上套用的主廚延伸。</span><span class="sxs-lookup"><span data-stu-id="8c850-106">The **Get-AzureVMChefExtension** cmdlet gets the Chef extension applied on a virtual machine.</span></span>

## <span data-ttu-id="8c850-107">示例</span><span class="sxs-lookup"><span data-stu-id="8c850-107">EXAMPLES</span></span>

### <span data-ttu-id="8c850-108">範例1：取得在指定的虛擬機器上套用的主廚延伸</span><span class="sxs-lookup"><span data-stu-id="8c850-108">Example 1: Get the Chef extension applied on the specified virtual machine</span></span>
```
PS C:\> Get-AzureVMChefExtension -VM $VM;
```

<span data-ttu-id="8c850-109">這個命令會取得在指定的虛擬機器上套用的主廚延伸。</span><span class="sxs-lookup"><span data-stu-id="8c850-109">This command gets the Chef extension applied on the specified virtual machine.</span></span>

## <span data-ttu-id="8c850-110">參數</span><span class="sxs-lookup"><span data-stu-id="8c850-110">PARAMETERS</span></span>

### <span data-ttu-id="8c850-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="8c850-111">-InformationAction</span></span>
<span data-ttu-id="8c850-112">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="8c850-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="8c850-113">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="8c850-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8c850-114">持續</span><span class="sxs-lookup"><span data-stu-id="8c850-114">Continue</span></span>
- <span data-ttu-id="8c850-115">理會</span><span class="sxs-lookup"><span data-stu-id="8c850-115">Ignore</span></span>
- <span data-ttu-id="8c850-116">看</span><span class="sxs-lookup"><span data-stu-id="8c850-116">Inquire</span></span>
- <span data-ttu-id="8c850-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="8c850-117">SilentlyContinue</span></span>
- <span data-ttu-id="8c850-118">停止</span><span class="sxs-lookup"><span data-stu-id="8c850-118">Stop</span></span>
- <span data-ttu-id="8c850-119">封存</span><span class="sxs-lookup"><span data-stu-id="8c850-119">Suspend</span></span>

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

### <span data-ttu-id="8c850-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="8c850-120">-InformationVariable</span></span>
<span data-ttu-id="8c850-121">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="8c850-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="8c850-122">-設定檔</span><span class="sxs-lookup"><span data-stu-id="8c850-122">-Profile</span></span>
<span data-ttu-id="8c850-123">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="8c850-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8c850-124">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="8c850-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8c850-125">-VM</span><span class="sxs-lookup"><span data-stu-id="8c850-125">-VM</span></span>
<span data-ttu-id="8c850-126">指定持久性虛擬電腦物件。</span><span class="sxs-lookup"><span data-stu-id="8c850-126">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="8c850-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c850-127">CommonParameters</span></span>
<span data-ttu-id="8c850-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8c850-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c850-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8c850-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c850-130">輸入</span><span class="sxs-lookup"><span data-stu-id="8c850-130">INPUTS</span></span>

## <span data-ttu-id="8c850-131">輸出</span><span class="sxs-lookup"><span data-stu-id="8c850-131">OUTPUTS</span></span>

## <span data-ttu-id="8c850-132">筆記</span><span class="sxs-lookup"><span data-stu-id="8c850-132">NOTES</span></span>

## <span data-ttu-id="8c850-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="8c850-133">RELATED LINKS</span></span>

[<span data-ttu-id="8c850-134">移除-AzureVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="8c850-134">Remove-AzureVMChefExtension</span></span>](./Remove-AzureVMChefExtension.md)

[<span data-ttu-id="8c850-135">Set-AzureVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="8c850-135">Set-AzureVMChefExtension</span></span>](./Set-AzureVMChefExtension.md)


