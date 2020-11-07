---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 48211644-1B92-443D-A992-BDF517D89341
online version: ''
schema: 2.0.0
ms.openlocfilehash: 49b4039e07cf9f393a85c9592598ad870586fd06
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/08/2020
ms.locfileid: "93968876"
---
# <span data-ttu-id="34cca-101">Get-WAPackVMSizeProfile</span><span class="sxs-lookup"><span data-stu-id="34cca-101">Get-WAPackVMSizeProfile</span></span>

## <span data-ttu-id="34cca-102">摘要</span><span class="sxs-lookup"><span data-stu-id="34cca-102">SYNOPSIS</span></span>
<span data-ttu-id="34cca-103">取得大小設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="34cca-103">Gets size profile objects.</span></span>

## <span data-ttu-id="34cca-104">句法</span><span class="sxs-lookup"><span data-stu-id="34cca-104">SYNTAX</span></span>

### <span data-ttu-id="34cca-105">空白 (預設) </span><span class="sxs-lookup"><span data-stu-id="34cca-105">Empty (Default)</span></span>
```
Get-WAPackVMSizeProfile [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="34cca-106">FromId</span><span class="sxs-lookup"><span data-stu-id="34cca-106">FromId</span></span>
```
Get-WAPackVMSizeProfile [-ID <Guid>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="34cca-107">FromName</span><span class="sxs-lookup"><span data-stu-id="34cca-107">FromName</span></span>
```
Get-WAPackVMSizeProfile [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="34cca-108">說明</span><span class="sxs-lookup"><span data-stu-id="34cca-108">DESCRIPTION</span></span>
<span data-ttu-id="34cca-109">這些主題已棄用，未來將會移除。</span><span class="sxs-lookup"><span data-stu-id="34cca-109">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="34cca-110">本主題描述 Microsoft Azure PowerShell 模組的0.8.1 版本中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="34cca-110">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="34cca-111">若要找出您正在使用的模組版本，請從 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。</span><span class="sxs-lookup"><span data-stu-id="34cca-111">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="34cca-112">**WAPackVMSizeProfile** Cmdlet 會取得虛擬機器的大小設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="34cca-112">The **Get-WAPackVMSizeProfile** cmdlet gets size profile objects for virtual machines.</span></span>

## <span data-ttu-id="34cca-113">示例</span><span class="sxs-lookup"><span data-stu-id="34cca-113">EXAMPLES</span></span>

### <span data-ttu-id="34cca-114">範例1：使用名稱取得大小設定檔</span><span class="sxs-lookup"><span data-stu-id="34cca-114">Example 1: Get a size profile by using a name</span></span>
```
PS C:\> Get-WAPackVMSizeProfile -Name "ContosoSizeProfile07"
```

<span data-ttu-id="34cca-115">這個命令會取得名為 ContosoSizeProfile07 的大小設定檔。</span><span class="sxs-lookup"><span data-stu-id="34cca-115">This command gets the size profile named ContosoSizeProfile07.</span></span>

### <span data-ttu-id="34cca-116">範例2：使用識別碼取得大小設定檔</span><span class="sxs-lookup"><span data-stu-id="34cca-116">Example 2: Get a size profile by using an ID</span></span>
```
PS C:\> Get-WAPackVMSizeProfile -ID 66242D17-189F-480D-87CF-8E1D749998C8
```

<span data-ttu-id="34cca-117">這個命令會取得具有指定識別碼的大小設定檔。</span><span class="sxs-lookup"><span data-stu-id="34cca-117">This command gets the size profile that has the specified ID.</span></span>

### <span data-ttu-id="34cca-118">範例3：取得所有大小設定檔</span><span class="sxs-lookup"><span data-stu-id="34cca-118">Example 3: Get all size profiles</span></span>
```
PS C:\> Get-WAPackVMSizeProfile
```

<span data-ttu-id="34cca-119">這個命令會取得所有大小設定檔。</span><span class="sxs-lookup"><span data-stu-id="34cca-119">This command gets all the size profiles.</span></span>

## <span data-ttu-id="34cca-120">參數</span><span class="sxs-lookup"><span data-stu-id="34cca-120">PARAMETERS</span></span>

### <span data-ttu-id="34cca-121">-識別碼</span><span class="sxs-lookup"><span data-stu-id="34cca-121">-ID</span></span>
<span data-ttu-id="34cca-122">指定大小設定檔的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="34cca-122">Specifies the unique ID of a size profile.</span></span>

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

### <span data-ttu-id="34cca-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="34cca-123">-Name</span></span>
<span data-ttu-id="34cca-124">指定大小設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="34cca-124">Specifies the name of a size profile.</span></span>

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

### <span data-ttu-id="34cca-125">-設定檔</span><span class="sxs-lookup"><span data-stu-id="34cca-125">-Profile</span></span>
<span data-ttu-id="34cca-126">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="34cca-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="34cca-127">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="34cca-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="34cca-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34cca-128">CommonParameters</span></span>
<span data-ttu-id="34cca-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="34cca-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34cca-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="34cca-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34cca-131">輸入</span><span class="sxs-lookup"><span data-stu-id="34cca-131">INPUTS</span></span>

## <span data-ttu-id="34cca-132">輸出</span><span class="sxs-lookup"><span data-stu-id="34cca-132">OUTPUTS</span></span>

## <span data-ttu-id="34cca-133">筆記</span><span class="sxs-lookup"><span data-stu-id="34cca-133">NOTES</span></span>

## <span data-ttu-id="34cca-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="34cca-134">RELATED LINKS</span></span>

[<span data-ttu-id="34cca-135">WAPackVM</span><span class="sxs-lookup"><span data-stu-id="34cca-135">Get-WAPackVM</span></span>](./Get-WAPackVM.md)


