---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: FEFBF1EF-FBCE-45D8-8455-F3F8662F1F36
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4ddf78f30cb6938571fc967d510e4ab99a0cfc80
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967833"
---
# <span data-ttu-id="90344-101">Add-AzurePHPWorkerRole</span><span class="sxs-lookup"><span data-stu-id="90344-101">Add-AzurePHPWorkerRole</span></span>

## <span data-ttu-id="90344-102">摘要</span><span class="sxs-lookup"><span data-stu-id="90344-102">SYNOPSIS</span></span>
<span data-ttu-id="90344-103">針對將由 php.exe 託管至 Azure 的 PHP 應用程式建立所需的檔案和配置。</span><span class="sxs-lookup"><span data-stu-id="90344-103">Creates the required files and configuration for a PHP application that will be hosted in Azure through php.exe.</span></span>

## <span data-ttu-id="90344-104">句法</span><span class="sxs-lookup"><span data-stu-id="90344-104">SYNTAX</span></span>

```
Add-AzurePHPWorkerRole [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="90344-105">說明</span><span class="sxs-lookup"><span data-stu-id="90344-105">DESCRIPTION</span></span>
<span data-ttu-id="90344-106">本主題描述 Microsoft Azure PowerShell 模組的0.8.10 版本中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="90344-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="90344-107">若要取得您正在使用的模組版本，請在 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。</span><span class="sxs-lookup"><span data-stu-id="90344-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="90344-108">針對將由 php.exe 託管至 Azure 的 PHP 應用程式，建立所需的檔案和設定（有時稱為基架）。</span><span class="sxs-lookup"><span data-stu-id="90344-108">Creates the required files and configuration, sometimes referred to as scaffolding, for a PHP application that will be hosted in Azure through php.exe.</span></span>

## <span data-ttu-id="90344-109">示例</span><span class="sxs-lookup"><span data-stu-id="90344-109">EXAMPLES</span></span>

### <span data-ttu-id="90344-110">範例1：使用單一實例建立 worker 角色</span><span class="sxs-lookup"><span data-stu-id="90344-110">Example 1: Create a worker role with a single instance</span></span>
```
PS C:\> Add-AzurePHPWorkerRole MyWorkerRole
```

<span data-ttu-id="90344-111">這個範例會將一個名為 MyWorkerRole 的單一輔助角色角色所需的檔案和配置新增至目前的應用程式。</span><span class="sxs-lookup"><span data-stu-id="90344-111">This example adds the required files and configuration for a single worker role named MyWorkerRole to the current application.</span></span>

### <span data-ttu-id="90344-112">範例2：建立具有多個實例的 worker 角色</span><span class="sxs-lookup"><span data-stu-id="90344-112">Example 2: Create a worker role with multiple instances</span></span>
```
PS C:\> Add-AzurePHPWorkerRole MyWorkerRole -I 2
```

<span data-ttu-id="90344-113">這個範例會將新的 worker 角色所需的檔案和配置新增至目前的應用程式，並使用 name MyWorkerRole，角色實例計數為2。</span><span class="sxs-lookup"><span data-stu-id="90344-113">This example adds the required files and configuration for a new worker role to the current application, using the name MyWorkerRole with a role instance count of 2.</span></span>

## <span data-ttu-id="90344-114">參數</span><span class="sxs-lookup"><span data-stu-id="90344-114">PARAMETERS</span></span>

### <span data-ttu-id="90344-115">-實例</span><span class="sxs-lookup"><span data-stu-id="90344-115">-Instances</span></span>
<span data-ttu-id="90344-116">指定此 worker 角色的角色實例數。</span><span class="sxs-lookup"><span data-stu-id="90344-116">Specifies the number of role instances for this worker role.</span></span>
<span data-ttu-id="90344-117">預設值為1。</span><span class="sxs-lookup"><span data-stu-id="90344-117">The default is 1.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: i

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90344-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="90344-118">-Name</span></span>
<span data-ttu-id="90344-119">指定 worker 角色的名稱。</span><span class="sxs-lookup"><span data-stu-id="90344-119">Specifies the name of the worker role.</span></span>
<span data-ttu-id="90344-120">名稱會決定包含在 worker 角色中託管之 PHP 服務所需的檔案和配置的資料夾名稱。</span><span class="sxs-lookup"><span data-stu-id="90344-120">The name determines the folder name that contains the required files and configuration for the PHP service hosted in the worker role.</span></span>
<span data-ttu-id="90344-121">預設值為 WorkerRole1。</span><span class="sxs-lookup"><span data-stu-id="90344-121">The default is WorkerRole1.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: n

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90344-122">-設定檔</span><span class="sxs-lookup"><span data-stu-id="90344-122">-Profile</span></span>
<span data-ttu-id="90344-123">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="90344-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="90344-124">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="90344-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="90344-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90344-125">CommonParameters</span></span>
<span data-ttu-id="90344-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="90344-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90344-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="90344-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90344-128">輸入</span><span class="sxs-lookup"><span data-stu-id="90344-128">INPUTS</span></span>

## <span data-ttu-id="90344-129">輸出</span><span class="sxs-lookup"><span data-stu-id="90344-129">OUTPUTS</span></span>

## <span data-ttu-id="90344-130">筆記</span><span class="sxs-lookup"><span data-stu-id="90344-130">NOTES</span></span>

## <span data-ttu-id="90344-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="90344-131">RELATED LINKS</span></span>

[<span data-ttu-id="90344-132">新-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="90344-132">New-AzureServiceProject</span></span>](./New-AzureServiceProject.md)

[<span data-ttu-id="90344-133">附加 AzurePHPWebRole</span><span class="sxs-lookup"><span data-stu-id="90344-133">Add-AzurePHPWebRole</span></span>](./Add-AzurePHPWebRole.md)


