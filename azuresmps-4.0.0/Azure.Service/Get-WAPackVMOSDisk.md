---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E6E40D1B-A5BC-4B38-9D22-F06A8E4DABDF
online version: ''
schema: 2.0.0
ms.openlocfilehash: f1360f45b751088bd899282cee2e64ce965d11fb
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/08/2020
ms.locfileid: "93968798"
---
# <span data-ttu-id="29db0-101">Get-WAPackVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="29db0-101">Get-WAPackVMOSDisk</span></span>

## <span data-ttu-id="29db0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="29db0-102">SYNOPSIS</span></span>
<span data-ttu-id="29db0-103">取得虛擬機器的作業系統磁片物件。</span><span class="sxs-lookup"><span data-stu-id="29db0-103">Gets operating system disk objects for virtual machines.</span></span>

## <span data-ttu-id="29db0-104">句法</span><span class="sxs-lookup"><span data-stu-id="29db0-104">SYNTAX</span></span>

### <span data-ttu-id="29db0-105">空白 (預設) </span><span class="sxs-lookup"><span data-stu-id="29db0-105">Empty (Default)</span></span>
```
Get-WAPackVMOSDisk [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="29db0-106">FromId</span><span class="sxs-lookup"><span data-stu-id="29db0-106">FromId</span></span>
```
Get-WAPackVMOSDisk [-ID <Guid>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="29db0-107">FromName</span><span class="sxs-lookup"><span data-stu-id="29db0-107">FromName</span></span>
```
Get-WAPackVMOSDisk [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="29db0-108">說明</span><span class="sxs-lookup"><span data-stu-id="29db0-108">DESCRIPTION</span></span>
<span data-ttu-id="29db0-109">這些主題已棄用，未來將會移除。</span><span class="sxs-lookup"><span data-stu-id="29db0-109">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="29db0-110">本主題描述 Microsoft Azure PowerShell 模組的0.8.1 版本中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="29db0-110">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="29db0-111">若要找出您正在使用的模組版本，請從 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。</span><span class="sxs-lookup"><span data-stu-id="29db0-111">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="29db0-112">**WAPackVMOSDisk** Cmdlet 會取得虛擬機器的作業系統磁片物件。</span><span class="sxs-lookup"><span data-stu-id="29db0-112">The **Get-WAPackVMOSDisk** cmdlet gets operating system disk objects for virtual machines.</span></span>

## <span data-ttu-id="29db0-113">示例</span><span class="sxs-lookup"><span data-stu-id="29db0-113">EXAMPLES</span></span>

### <span data-ttu-id="29db0-114">範例1：使用名稱取得作業系統磁片</span><span class="sxs-lookup"><span data-stu-id="29db0-114">Example 1: Get an operating system disk by using a name</span></span>
```
PS C:\> Get-WAPackVMOSDisk -Name "ContosoOSDisk"
```

<span data-ttu-id="29db0-115">這個命令會取得一個名為 ContosoOSDisk 的作業系統磁片。</span><span class="sxs-lookup"><span data-stu-id="29db0-115">This command gets an operating system disk named ContosoOSDisk.</span></span>

### <span data-ttu-id="29db0-116">範例2：使用識別碼取得作業系統磁片</span><span class="sxs-lookup"><span data-stu-id="29db0-116">Example 2: Get an operating system disk by using an ID</span></span>
```
PS C:\> Get-WAPackVMOSDisk -Id 66242D17-189F-480D-87CF-8E1D749998C8
```

<span data-ttu-id="29db0-117">這個命令會取得具有指定識別碼的作業系統磁片。</span><span class="sxs-lookup"><span data-stu-id="29db0-117">This command gets the operating system disk that has the specified ID.</span></span>

### <span data-ttu-id="29db0-118">範例3：取得所有作業系統磁片</span><span class="sxs-lookup"><span data-stu-id="29db0-118">Example 3: Get all operating system disks</span></span>
```
PS C:\> Get-WAPackVMOSDisk
```

<span data-ttu-id="29db0-119">這個命令會取得所有作業系統磁片。</span><span class="sxs-lookup"><span data-stu-id="29db0-119">This command gets all operating system disks.</span></span>

## <span data-ttu-id="29db0-120">參數</span><span class="sxs-lookup"><span data-stu-id="29db0-120">PARAMETERS</span></span>

### <span data-ttu-id="29db0-121">-識別碼</span><span class="sxs-lookup"><span data-stu-id="29db0-121">-ID</span></span>
<span data-ttu-id="29db0-122">指定作業系統磁片的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="29db0-122">Specifies the unique ID of an operating system disk.</span></span>

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

### <span data-ttu-id="29db0-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="29db0-123">-Name</span></span>
<span data-ttu-id="29db0-124">指定作業系統磁片的名稱。</span><span class="sxs-lookup"><span data-stu-id="29db0-124">Specifies the name of an operating system disk.</span></span>

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

### <span data-ttu-id="29db0-125">-設定檔</span><span class="sxs-lookup"><span data-stu-id="29db0-125">-Profile</span></span>
<span data-ttu-id="29db0-126">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="29db0-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="29db0-127">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="29db0-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="29db0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29db0-128">CommonParameters</span></span>
<span data-ttu-id="29db0-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="29db0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29db0-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="29db0-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29db0-131">輸入</span><span class="sxs-lookup"><span data-stu-id="29db0-131">INPUTS</span></span>

## <span data-ttu-id="29db0-132">輸出</span><span class="sxs-lookup"><span data-stu-id="29db0-132">OUTPUTS</span></span>

## <span data-ttu-id="29db0-133">筆記</span><span class="sxs-lookup"><span data-stu-id="29db0-133">NOTES</span></span>

## <span data-ttu-id="29db0-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="29db0-134">RELATED LINKS</span></span>

[<span data-ttu-id="29db0-135">WAPackVM</span><span class="sxs-lookup"><span data-stu-id="29db0-135">Get-WAPackVM</span></span>](./Get-WAPackVM.md)


