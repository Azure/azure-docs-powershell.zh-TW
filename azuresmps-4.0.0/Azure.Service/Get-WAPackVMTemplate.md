---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 37C788AC-B369-432B-8276-27FFB0B4CF10
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8d2913877a9f68621bb5c1c930443a46e91e5935
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/08/2020
ms.locfileid: "93968837"
---
# <span data-ttu-id="cebe4-101">Get-WAPackVMTemplate</span><span class="sxs-lookup"><span data-stu-id="cebe4-101">Get-WAPackVMTemplate</span></span>

## <span data-ttu-id="cebe4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cebe4-102">SYNOPSIS</span></span>
<span data-ttu-id="cebe4-103">取得虛擬機器範本。</span><span class="sxs-lookup"><span data-stu-id="cebe4-103">Gets virtual machine templates.</span></span>

## <span data-ttu-id="cebe4-104">句法</span><span class="sxs-lookup"><span data-stu-id="cebe4-104">SYNTAX</span></span>

### <span data-ttu-id="cebe4-105">空白 (預設) </span><span class="sxs-lookup"><span data-stu-id="cebe4-105">Empty (Default)</span></span>
```
Get-WAPackVMTemplate [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="cebe4-106">FromId</span><span class="sxs-lookup"><span data-stu-id="cebe4-106">FromId</span></span>
```
Get-WAPackVMTemplate [-ID <Guid>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="cebe4-107">FromName</span><span class="sxs-lookup"><span data-stu-id="cebe4-107">FromName</span></span>
```
Get-WAPackVMTemplate [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="cebe4-108">說明</span><span class="sxs-lookup"><span data-stu-id="cebe4-108">DESCRIPTION</span></span>
<span data-ttu-id="cebe4-109">這些主題已棄用，未來將會移除。</span><span class="sxs-lookup"><span data-stu-id="cebe4-109">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="cebe4-110">本主題描述 Microsoft Azure PowerShell 模組的0.8.1 版本中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cebe4-110">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="cebe4-111">若要找出您正在使用的模組版本，請從 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。</span><span class="sxs-lookup"><span data-stu-id="cebe4-111">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="cebe4-112">**WAPackVMTemplate** Cmdlet 會取得虛擬機器範本。</span><span class="sxs-lookup"><span data-stu-id="cebe4-112">The **Get-WAPackVMTemplate** cmdlet gets virtual machine templates.</span></span>

## <span data-ttu-id="cebe4-113">示例</span><span class="sxs-lookup"><span data-stu-id="cebe4-113">EXAMPLES</span></span>

### <span data-ttu-id="cebe4-114">範例1：使用名稱取得虛擬機器範本</span><span class="sxs-lookup"><span data-stu-id="cebe4-114">Example 1: Get a virtual machine template by using a name</span></span>
```
PS C:\> Get-WAPackVMTemplate -Name "ContosoTemplate04"
```

<span data-ttu-id="cebe4-115">這個命令會取得名為 ContosoTemplate04 的虛擬機器範本。</span><span class="sxs-lookup"><span data-stu-id="cebe4-115">This command gets the virtual machine template named ContosoTemplate04.</span></span>

### <span data-ttu-id="cebe4-116">範例2：使用識別碼取得虛擬機器範本</span><span class="sxs-lookup"><span data-stu-id="cebe4-116">Example 2: Get a virtual machine template by using an ID</span></span>
```
PS C:\> Get-WAPackVMTemplate -Id 66242D17-189F-480D-87CF-8E1D749998C8
```

<span data-ttu-id="cebe4-117">這個命令會取得具有指定識別碼的虛擬機器範本。</span><span class="sxs-lookup"><span data-stu-id="cebe4-117">This command gets the virtual machine template that has the specified ID.</span></span>

### <span data-ttu-id="cebe4-118">範例3：取得所有虛擬機器範本</span><span class="sxs-lookup"><span data-stu-id="cebe4-118">Example 3: Get all virtual machine templates</span></span>
```
PS C:\> Get-WAPackVMTemplate
```

<span data-ttu-id="cebe4-119">這個命令會取得所有的虛擬機器範本。</span><span class="sxs-lookup"><span data-stu-id="cebe4-119">This command gets all the virtual machine templates.</span></span>

## <span data-ttu-id="cebe4-120">參數</span><span class="sxs-lookup"><span data-stu-id="cebe4-120">PARAMETERS</span></span>

### <span data-ttu-id="cebe4-121">-識別碼</span><span class="sxs-lookup"><span data-stu-id="cebe4-121">-ID</span></span>
<span data-ttu-id="cebe4-122">指定範本的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="cebe4-122">Specifies the unique ID of a template.</span></span>

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

### <span data-ttu-id="cebe4-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="cebe4-123">-Name</span></span>
<span data-ttu-id="cebe4-124">指定範本的名稱。</span><span class="sxs-lookup"><span data-stu-id="cebe4-124">Specifies the name of a template.</span></span>

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

### <span data-ttu-id="cebe4-125">-設定檔</span><span class="sxs-lookup"><span data-stu-id="cebe4-125">-Profile</span></span>
<span data-ttu-id="cebe4-126">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="cebe4-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="cebe4-127">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="cebe4-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="cebe4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cebe4-128">CommonParameters</span></span>
<span data-ttu-id="cebe4-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cebe4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cebe4-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cebe4-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cebe4-131">輸入</span><span class="sxs-lookup"><span data-stu-id="cebe4-131">INPUTS</span></span>

## <span data-ttu-id="cebe4-132">輸出</span><span class="sxs-lookup"><span data-stu-id="cebe4-132">OUTPUTS</span></span>

## <span data-ttu-id="cebe4-133">筆記</span><span class="sxs-lookup"><span data-stu-id="cebe4-133">NOTES</span></span>

## <span data-ttu-id="cebe4-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="cebe4-134">RELATED LINKS</span></span>

[<span data-ttu-id="cebe4-135">WAPackVM</span><span class="sxs-lookup"><span data-stu-id="cebe4-135">Get-WAPackVM</span></span>](./Get-WAPackVM.md)


