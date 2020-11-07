---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 78099E89-63C9-4019-A4ED-EF37D2383A09
online version: ''
schema: 2.0.0
ms.openlocfilehash: 23e6165e50c227320875fa70e97d63b0cdd78781
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967123"
---
# <span data-ttu-id="54cf2-101">Export-AzureVM</span><span class="sxs-lookup"><span data-stu-id="54cf2-101">Export-AzureVM</span></span>

## <span data-ttu-id="54cf2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="54cf2-102">SYNOPSIS</span></span>
<span data-ttu-id="54cf2-103">匯出 Azure 虛擬機器狀態至檔案。</span><span class="sxs-lookup"><span data-stu-id="54cf2-103">Exports an Azure virtual machine state to a file.</span></span>

## <span data-ttu-id="54cf2-104">句法</span><span class="sxs-lookup"><span data-stu-id="54cf2-104">SYNTAX</span></span>

```
Export-AzureVM [-ServiceName] <String> [-Name] <String> [-Path] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="54cf2-105">說明</span><span class="sxs-lookup"><span data-stu-id="54cf2-105">DESCRIPTION</span></span>
<span data-ttu-id="54cf2-106">**Export-add-azurevm** Cmdlet 會將虛擬機器的狀態匯出為 .xml 檔案。</span><span class="sxs-lookup"><span data-stu-id="54cf2-106">The **Export-AzureVM** cmdlet exports the state of a virtual machine to an .xml file.</span></span>

<span data-ttu-id="54cf2-107">執行 **Export** ，接著再按下 **Remove** ，然後按下 **add-azurevm** 來重新建立虛擬機器，可能會導致產生的虛擬機器與原始的 IP 位址不同。</span><span class="sxs-lookup"><span data-stu-id="54cf2-107">Running **Export-AzureVM** , followed by **Remove-AzureVM** and then **Import-AzureVM** to recreate a virtual machine can cause the resultant virtual machine to have a different IP address than the original.</span></span>

## <span data-ttu-id="54cf2-108">示例</span><span class="sxs-lookup"><span data-stu-id="54cf2-108">EXAMPLES</span></span>

### <span data-ttu-id="54cf2-109">範例1：匯出虛擬機器</span><span class="sxs-lookup"><span data-stu-id="54cf2-109">Example 1: Export a virtual machine</span></span>
```
PS C:\> Export-AzureVM -ServiceName "ContosoService" -Name "ContosoRole06" -Path "C:\vms\VMstate.xml"
```

<span data-ttu-id="54cf2-110">這個命令會將指定的虛擬機器狀態匯出至 VMstate.xml 檔案。</span><span class="sxs-lookup"><span data-stu-id="54cf2-110">This command exports the state of the specified virtual machine to the VMstate.xml file.</span></span>

## <span data-ttu-id="54cf2-111">參數</span><span class="sxs-lookup"><span data-stu-id="54cf2-111">PARAMETERS</span></span>

### <span data-ttu-id="54cf2-112">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="54cf2-112">-InformationAction</span></span>
<span data-ttu-id="54cf2-113">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="54cf2-113">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="54cf2-114">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="54cf2-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="54cf2-115">持續</span><span class="sxs-lookup"><span data-stu-id="54cf2-115">Continue</span></span>
- <span data-ttu-id="54cf2-116">理會</span><span class="sxs-lookup"><span data-stu-id="54cf2-116">Ignore</span></span>
- <span data-ttu-id="54cf2-117">看</span><span class="sxs-lookup"><span data-stu-id="54cf2-117">Inquire</span></span>
- <span data-ttu-id="54cf2-118">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="54cf2-118">SilentlyContinue</span></span>
- <span data-ttu-id="54cf2-119">停止</span><span class="sxs-lookup"><span data-stu-id="54cf2-119">Stop</span></span>
- <span data-ttu-id="54cf2-120">封存</span><span class="sxs-lookup"><span data-stu-id="54cf2-120">Suspend</span></span>

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

### <span data-ttu-id="54cf2-121">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="54cf2-121">-InformationVariable</span></span>
<span data-ttu-id="54cf2-122">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="54cf2-122">Specifies an information variable.</span></span>

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

### <span data-ttu-id="54cf2-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="54cf2-123">-Name</span></span>
<span data-ttu-id="54cf2-124">指定此 Cmdlet 匯出狀態的虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="54cf2-124">Specifies the name of the virtual machine for which this cmdlet exports state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54cf2-125">-Path</span><span class="sxs-lookup"><span data-stu-id="54cf2-125">-Path</span></span>
<span data-ttu-id="54cf2-126">指定此 Cmdlet 儲存虛擬機器狀態的路徑和檔案名。</span><span class="sxs-lookup"><span data-stu-id="54cf2-126">Specifies the path and file name to which this cmdlet saves the virtual machine state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54cf2-127">-設定檔</span><span class="sxs-lookup"><span data-stu-id="54cf2-127">-Profile</span></span>
<span data-ttu-id="54cf2-128">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="54cf2-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="54cf2-129">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="54cf2-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="54cf2-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="54cf2-130">-ServiceName</span></span>
<span data-ttu-id="54cf2-131">指定託管虛擬機器的 Azure 服務名稱。</span><span class="sxs-lookup"><span data-stu-id="54cf2-131">Specifies the name of the Azure service that hosts the virtual machine.</span></span>

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

### <span data-ttu-id="54cf2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54cf2-132">CommonParameters</span></span>
<span data-ttu-id="54cf2-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="54cf2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54cf2-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="54cf2-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54cf2-135">輸入</span><span class="sxs-lookup"><span data-stu-id="54cf2-135">INPUTS</span></span>

## <span data-ttu-id="54cf2-136">輸出</span><span class="sxs-lookup"><span data-stu-id="54cf2-136">OUTPUTS</span></span>

## <span data-ttu-id="54cf2-137">筆記</span><span class="sxs-lookup"><span data-stu-id="54cf2-137">NOTES</span></span>

## <span data-ttu-id="54cf2-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="54cf2-138">RELATED LINKS</span></span>

[<span data-ttu-id="54cf2-139">Import-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="54cf2-139">Import-AzureVM</span></span>](./Import-AzureVM.md)


