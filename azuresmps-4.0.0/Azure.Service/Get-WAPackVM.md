---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 047C5FBD-CB0D-47BF-AE03-4DF32B4FAD87
online version: ''
schema: 2.0.0
ms.openlocfilehash: a546c9fdb066aaf1203055fd62d8eb01258569c8
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/08/2020
ms.locfileid: "93968802"
---
# <span data-ttu-id="5dd63-101">Get-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="5dd63-101">Get-WAPackVM</span></span>

## <span data-ttu-id="5dd63-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5dd63-102">SYNOPSIS</span></span>
<span data-ttu-id="5dd63-103">取得虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="5dd63-103">Gets virtual machine objects.</span></span>

## <span data-ttu-id="5dd63-104">句法</span><span class="sxs-lookup"><span data-stu-id="5dd63-104">SYNTAX</span></span>

### <span data-ttu-id="5dd63-105">空白 (預設) </span><span class="sxs-lookup"><span data-stu-id="5dd63-105">Empty (Default)</span></span>
```
Get-WAPackVM [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="5dd63-106">FromName</span><span class="sxs-lookup"><span data-stu-id="5dd63-106">FromName</span></span>
```
Get-WAPackVM [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="5dd63-107">FromId</span><span class="sxs-lookup"><span data-stu-id="5dd63-107">FromId</span></span>
```
Get-WAPackVM [-ID <Guid>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="5dd63-108">說明</span><span class="sxs-lookup"><span data-stu-id="5dd63-108">DESCRIPTION</span></span>
<span data-ttu-id="5dd63-109">這些主題已棄用，未來將會移除。</span><span class="sxs-lookup"><span data-stu-id="5dd63-109">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="5dd63-110">本主題描述 Microsoft Azure PowerShell 模組的0.8.1 版本中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5dd63-110">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="5dd63-111">若要找出您正在使用的模組版本，請從 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。</span><span class="sxs-lookup"><span data-stu-id="5dd63-111">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="5dd63-112">**WAPackVM** Cmdlet 會取得虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="5dd63-112">The **Get-WAPackVM** cmdlet gets virtual machine objects.</span></span>

## <span data-ttu-id="5dd63-113">示例</span><span class="sxs-lookup"><span data-stu-id="5dd63-113">EXAMPLES</span></span>

### <span data-ttu-id="5dd63-114">範例1：使用名稱取得虛擬機器</span><span class="sxs-lookup"><span data-stu-id="5dd63-114">Example 1: Get a virtual machine by using a name</span></span>
```
PS C:\> Get-WAPackVM -Name "ContosoV126"
```

<span data-ttu-id="5dd63-115">這個命令會取得名為 ContosoV126 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="5dd63-115">This command gets the virtual machine named ContosoV126.</span></span>

### <span data-ttu-id="5dd63-116">範例2：使用識別碼取得虛擬機器</span><span class="sxs-lookup"><span data-stu-id="5dd63-116">Example 2: Get a virtual machine by using an ID</span></span>
```
PS C:\> Get-WAPackVM -Id 66242D17-189F-480D-87CF-8E1D749998C8
```

<span data-ttu-id="5dd63-117">這個命令會取得具有指定識別碼的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="5dd63-117">This command gets the virtual machine that has the specified ID.</span></span>

### <span data-ttu-id="5dd63-118">範例3：取得所有虛擬機器</span><span class="sxs-lookup"><span data-stu-id="5dd63-118">Example 3: Get all virtual machines</span></span>
```
PS C:\> Get-WAPackVM
```

<span data-ttu-id="5dd63-119">這個命令會取得所有的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="5dd63-119">This command gets all virtual machines.</span></span>

## <span data-ttu-id="5dd63-120">參數</span><span class="sxs-lookup"><span data-stu-id="5dd63-120">PARAMETERS</span></span>

### <span data-ttu-id="5dd63-121">-識別碼</span><span class="sxs-lookup"><span data-stu-id="5dd63-121">-ID</span></span>
<span data-ttu-id="5dd63-122">指定虛擬機器的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="5dd63-122">Specifies the unique ID of a virtual machine.</span></span>

```yaml
Type: Guid
Parameter Sets: FromId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5dd63-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="5dd63-123">-Name</span></span>
<span data-ttu-id="5dd63-124">指定虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="5dd63-124">Specifies the name of a virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: FromName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5dd63-125">-設定檔</span><span class="sxs-lookup"><span data-stu-id="5dd63-125">-Profile</span></span>
<span data-ttu-id="5dd63-126">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="5dd63-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5dd63-127">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="5dd63-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5dd63-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5dd63-128">CommonParameters</span></span>
<span data-ttu-id="5dd63-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5dd63-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5dd63-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5dd63-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5dd63-131">輸入</span><span class="sxs-lookup"><span data-stu-id="5dd63-131">INPUTS</span></span>

## <span data-ttu-id="5dd63-132">輸出</span><span class="sxs-lookup"><span data-stu-id="5dd63-132">OUTPUTS</span></span>

## <span data-ttu-id="5dd63-133">筆記</span><span class="sxs-lookup"><span data-stu-id="5dd63-133">NOTES</span></span>

## <span data-ttu-id="5dd63-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="5dd63-134">RELATED LINKS</span></span>

[<span data-ttu-id="5dd63-135">新-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="5dd63-135">New-WAPackVM</span></span>](./New-WAPackVM.md)

[<span data-ttu-id="5dd63-136">移除-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="5dd63-136">Remove-WAPackVM</span></span>](./Remove-WAPackVM.md)

[<span data-ttu-id="5dd63-137">重新開機-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="5dd63-137">Restart-WAPackVM</span></span>](./Restart-WAPackVM.md)

[<span data-ttu-id="5dd63-138">Resume-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="5dd63-138">Resume-WAPackVM</span></span>](./Resume-WAPackVM.md)

[<span data-ttu-id="5dd63-139">Set-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="5dd63-139">Set-WAPackVM</span></span>](./Set-WAPackVM.md)

[<span data-ttu-id="5dd63-140">開始-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="5dd63-140">Start-WAPackVM</span></span>](./Start-WAPackVM.md)

[<span data-ttu-id="5dd63-141">停止 WAPackVM</span><span class="sxs-lookup"><span data-stu-id="5dd63-141">Stop-WAPackVM</span></span>](./Stop-WAPackVM.md)

[<span data-ttu-id="5dd63-142">暫停-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="5dd63-142">Suspend-WAPackVM</span></span>](./Suspend-WAPackVM.md)

[<span data-ttu-id="5dd63-143">WAPackVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="5dd63-143">Get-WAPackVMOSDisk</span></span>](./Get-WAPackVMOSDisk.md)


