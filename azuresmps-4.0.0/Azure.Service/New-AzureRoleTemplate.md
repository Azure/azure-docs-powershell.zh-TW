---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E499868E-A745-4CA4-A717-C33C3B94A2C8
online version: ''
schema: 2.0.0
ms.openlocfilehash: b80071bb82ebbb960be5b5b4fcc854dc47c9ed9d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967438"
---
# <span data-ttu-id="b96ab-101">New-AzureRoleTemplate</span><span class="sxs-lookup"><span data-stu-id="b96ab-101">New-AzureRoleTemplate</span></span>

## <span data-ttu-id="b96ab-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b96ab-102">SYNOPSIS</span></span>
<span data-ttu-id="b96ab-103">建立網站和 worker 角色範本。</span><span class="sxs-lookup"><span data-stu-id="b96ab-103">Creates web and worker role templates.</span></span>

## <span data-ttu-id="b96ab-104">句法</span><span class="sxs-lookup"><span data-stu-id="b96ab-104">SYNTAX</span></span>

### <span data-ttu-id="b96ab-105">WebRole</span><span class="sxs-lookup"><span data-stu-id="b96ab-105">WebRole</span></span>
```
New-AzureRoleTemplate [-Web] [-Output <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="b96ab-106">WorkerRole</span><span class="sxs-lookup"><span data-stu-id="b96ab-106">WorkerRole</span></span>
```
New-AzureRoleTemplate [-Worker] [-Output <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b96ab-107">說明</span><span class="sxs-lookup"><span data-stu-id="b96ab-107">DESCRIPTION</span></span>
<span data-ttu-id="b96ab-108">本主題描述 Microsoft Azure PowerShell 模組的0.8.10 版本中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b96ab-108">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="b96ab-109">若要取得您正在使用的模組版本，請在 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。</span><span class="sxs-lookup"><span data-stu-id="b96ab-109">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="b96ab-110">**AzureRoleTemplate** Cmdlet 會建立網站和 worker 角色範本。</span><span class="sxs-lookup"><span data-stu-id="b96ab-110">The **New-AzureRoleTemplate** cmdlet creates web and worker role templates.</span></span>

## <span data-ttu-id="b96ab-111">示例</span><span class="sxs-lookup"><span data-stu-id="b96ab-111">EXAMPLES</span></span>

### <span data-ttu-id="b96ab-112">範例1：建立網頁角色範本</span><span class="sxs-lookup"><span data-stu-id="b96ab-112">Example 1: Create a web role template</span></span>
```
PS C:\> New-AzureRoleTemplate -Web
```

<span data-ttu-id="b96ab-113">這個範例會在目前目錄中名為 WebRoleTemplate 的資料夾中建立新的網頁角色範本。</span><span class="sxs-lookup"><span data-stu-id="b96ab-113">This example creates a new web role template in a folder named WebRoleTemplate in the current directory.</span></span>

### <span data-ttu-id="b96ab-114">範例2：建立 worker 角色範本</span><span class="sxs-lookup"><span data-stu-id="b96ab-114">Example 2: Create a worker role template</span></span>
```
PS C:\> New-AzureRoleTemplate -Worker
```

<span data-ttu-id="b96ab-115">這個範例會在目前目錄中名為 WebRoleTemplate 的資料夾中建立新的輔助角色範本。</span><span class="sxs-lookup"><span data-stu-id="b96ab-115">This example creates a new worker role template in a folder named WebRoleTemplate in the current directory.</span></span>

### <span data-ttu-id="b96ab-116">範例3：在自訂目錄中建立角色範本</span><span class="sxs-lookup"><span data-stu-id="b96ab-116">Example 3: Create a role template in a custom directory</span></span>
```
PS C:\> New-AzureRoleTemplate -Web -Output C:\MyWebRoleTemplate
```

<span data-ttu-id="b96ab-117">這個範例會在名為 MyWebRoleTemplate 的目錄中建立新的網頁角色範本，而不是在目前的目錄中。</span><span class="sxs-lookup"><span data-stu-id="b96ab-117">This example creates a new web role template in directory named MyWebRoleTemplate, instead of in the current directory.</span></span>

## <span data-ttu-id="b96ab-118">參數</span><span class="sxs-lookup"><span data-stu-id="b96ab-118">PARAMETERS</span></span>

### <span data-ttu-id="b96ab-119">-輸出</span><span class="sxs-lookup"><span data-stu-id="b96ab-119">-Output</span></span>
<span data-ttu-id="b96ab-120">指定所產生範本的輸出路徑。</span><span class="sxs-lookup"><span data-stu-id="b96ab-120">Specifies the output path of generated template.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b96ab-121">-設定檔</span><span class="sxs-lookup"><span data-stu-id="b96ab-121">-Profile</span></span>
<span data-ttu-id="b96ab-122">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="b96ab-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b96ab-123">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="b96ab-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b96ab-124">網頁</span><span class="sxs-lookup"><span data-stu-id="b96ab-124">-Web</span></span>
<span data-ttu-id="b96ab-125">指定您要建立網頁角色範本。</span><span class="sxs-lookup"><span data-stu-id="b96ab-125">Specifies that you want to create a web role template.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WebRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b96ab-126">-員工</span><span class="sxs-lookup"><span data-stu-id="b96ab-126">-Worker</span></span>
<span data-ttu-id="b96ab-127">指定您要建立 worker 角色範本。</span><span class="sxs-lookup"><span data-stu-id="b96ab-127">Specifies that you want to create a worker role template.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WorkerRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b96ab-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b96ab-128">CommonParameters</span></span>
<span data-ttu-id="b96ab-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b96ab-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b96ab-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b96ab-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b96ab-131">輸入</span><span class="sxs-lookup"><span data-stu-id="b96ab-131">INPUTS</span></span>

## <span data-ttu-id="b96ab-132">輸出</span><span class="sxs-lookup"><span data-stu-id="b96ab-132">OUTPUTS</span></span>

## <span data-ttu-id="b96ab-133">筆記</span><span class="sxs-lookup"><span data-stu-id="b96ab-133">NOTES</span></span>

## <span data-ttu-id="b96ab-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="b96ab-134">RELATED LINKS</span></span>

[<span data-ttu-id="b96ab-135">附加 AzureWebRole</span><span class="sxs-lookup"><span data-stu-id="b96ab-135">Add-AzureWebRole</span></span>](./Add-AzureWebRole.md)

[<span data-ttu-id="b96ab-136">附加 AzureWorkerRole</span><span class="sxs-lookup"><span data-stu-id="b96ab-136">Add-AzureWorkerRole</span></span>](./Add-AzureWorkerRole.md)


