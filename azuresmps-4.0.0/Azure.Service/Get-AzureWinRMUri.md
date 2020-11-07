---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 5F827BFB-492E-48A2-9610-0CB5FBDD1F9E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0c66043fa36620c2879e88b7dbf82ba251aa4fbc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967951"
---
# <span data-ttu-id="5bd37-101">Get-AzureWinRMUri</span><span class="sxs-lookup"><span data-stu-id="5bd37-101">Get-AzureWinRMUri</span></span>

## <span data-ttu-id="5bd37-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5bd37-102">SYNOPSIS</span></span>
<span data-ttu-id="5bd37-103">取得指向虛擬機器或託管服務中虛擬機器清單的 WinRM HTTPs 偵聽程式 URI。</span><span class="sxs-lookup"><span data-stu-id="5bd37-103">Gets the URI to WinRM https listener to a virtual machine or a list of virtual machines in a hosted service.</span></span>

## <span data-ttu-id="5bd37-104">句法</span><span class="sxs-lookup"><span data-stu-id="5bd37-104">SYNTAX</span></span>

```
Get-AzureWinRMUri [-ServiceName] <String> [[-Name] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="5bd37-105">說明</span><span class="sxs-lookup"><span data-stu-id="5bd37-105">DESCRIPTION</span></span>
<span data-ttu-id="5bd37-106">**AzureWinRMUri** Cmdlet 會取得 Windows 遠端系統管理 (WinRM) HTTPs 偵聽程式的 URI，以加入託管服務中的虛擬機器或虛擬機器清單。</span><span class="sxs-lookup"><span data-stu-id="5bd37-106">The **Get-AzureWinRMUri** cmdlet gets the URI of the Windows Remote Management (WinRM) https listener to a virtual machine or a list of virtual machines in a hosted service.</span></span>

## <span data-ttu-id="5bd37-107">示例</span><span class="sxs-lookup"><span data-stu-id="5bd37-107">EXAMPLES</span></span>

### <span data-ttu-id="5bd37-108">範例1：取得 WinRM HTTPs 偵聽程式的 URI 至虛擬機器</span><span class="sxs-lookup"><span data-stu-id="5bd37-108">Example 1: Get the URI of the WinRM https listener to a virtual machine</span></span>
```
PS C:\> Get-AzureWinRMUri -ServiceName MyService -Name MyVM
```

<span data-ttu-id="5bd37-109">這個命令會取得 WinRM HTTPs 偵聽程式的 UIR 至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="5bd37-109">This command gets the UIR of the WinRM https listener to a virtual machine.</span></span>

### <span data-ttu-id="5bd37-110">範例2：取得 WinRM HTTPs 偵聽程式的 URI 至特定服務的虛擬機器</span><span class="sxs-lookup"><span data-stu-id="5bd37-110">Example 2: Get the URI of the WinRM https listener to a virtual machine of a specific service</span></span>
```
PS C:\> Get-AzureWinRMUri -ServiceName MyService
```

<span data-ttu-id="5bd37-111">這個命令會取得 WinRM HTTPs 偵聽程式的 UIR 至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="5bd37-111">This command gets the UIR of the WinRM https listener to a virtual machine.</span></span>

## <span data-ttu-id="5bd37-112">參數</span><span class="sxs-lookup"><span data-stu-id="5bd37-112">PARAMETERS</span></span>

### <span data-ttu-id="5bd37-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="5bd37-113">-InformationAction</span></span>
<span data-ttu-id="5bd37-114">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="5bd37-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="5bd37-115">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="5bd37-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5bd37-116">持續</span><span class="sxs-lookup"><span data-stu-id="5bd37-116">Continue</span></span>
- <span data-ttu-id="5bd37-117">理會</span><span class="sxs-lookup"><span data-stu-id="5bd37-117">Ignore</span></span>
- <span data-ttu-id="5bd37-118">看</span><span class="sxs-lookup"><span data-stu-id="5bd37-118">Inquire</span></span>
- <span data-ttu-id="5bd37-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="5bd37-119">SilentlyContinue</span></span>
- <span data-ttu-id="5bd37-120">停止</span><span class="sxs-lookup"><span data-stu-id="5bd37-120">Stop</span></span>
- <span data-ttu-id="5bd37-121">封存</span><span class="sxs-lookup"><span data-stu-id="5bd37-121">Suspend</span></span>

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

### <span data-ttu-id="5bd37-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="5bd37-122">-InformationVariable</span></span>
<span data-ttu-id="5bd37-123">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="5bd37-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="5bd37-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="5bd37-124">-Name</span></span>
<span data-ttu-id="5bd37-125">指定要為其產生 WinRM URI 的虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="5bd37-125">Specifies the name of the virtual machine to which the WinRM URI is generated.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bd37-126">-設定檔</span><span class="sxs-lookup"><span data-stu-id="5bd37-126">-Profile</span></span>
<span data-ttu-id="5bd37-127">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="5bd37-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5bd37-128">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="5bd37-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5bd37-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="5bd37-129">-ServiceName</span></span>
<span data-ttu-id="5bd37-130">指定託管虛擬機器的 Microsoft Azure 服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="5bd37-130">Specifies the name of the Microsoft Azure service that hosts the virtual machine.</span></span>

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

### <span data-ttu-id="5bd37-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bd37-131">CommonParameters</span></span>
<span data-ttu-id="5bd37-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5bd37-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bd37-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5bd37-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bd37-134">輸入</span><span class="sxs-lookup"><span data-stu-id="5bd37-134">INPUTS</span></span>

## <span data-ttu-id="5bd37-135">輸出</span><span class="sxs-lookup"><span data-stu-id="5bd37-135">OUTPUTS</span></span>

## <span data-ttu-id="5bd37-136">筆記</span><span class="sxs-lookup"><span data-stu-id="5bd37-136">NOTES</span></span>

## <span data-ttu-id="5bd37-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="5bd37-137">RELATED LINKS</span></span>

[<span data-ttu-id="5bd37-138">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="5bd37-138">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="5bd37-139">新-AzureQuickVM</span><span class="sxs-lookup"><span data-stu-id="5bd37-139">New-AzureQuickVM</span></span>](./New-AzureQuickVM.md)


