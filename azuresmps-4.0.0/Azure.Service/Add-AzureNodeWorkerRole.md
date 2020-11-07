---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 7190C668-6A0C-4E1D-9B5A-0CEEF53E3F85
online version: ''
schema: 2.0.0
ms.openlocfilehash: 93573caf43a6c711e1aa1308c851c82faaef5bcd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967835"
---
# <span data-ttu-id="ff87d-101">Add-AzureNodeWorkerRole</span><span class="sxs-lookup"><span data-stu-id="ff87d-101">Add-AzureNodeWorkerRole</span></span>

## <span data-ttu-id="ff87d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ff87d-102">SYNOPSIS</span></span>
<span data-ttu-id="ff87d-103">建立 Node.js 應用程式所需的檔案和資料夾，以便透過 node.exe 在雲端中託管</span><span class="sxs-lookup"><span data-stu-id="ff87d-103">Creates the required files and folders for a Node.js application to be hosted in the cloud via node.exe</span></span>

## <span data-ttu-id="ff87d-104">句法</span><span class="sxs-lookup"><span data-stu-id="ff87d-104">SYNTAX</span></span>

```
Add-AzureNodeWorkerRole [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ff87d-105">說明</span><span class="sxs-lookup"><span data-stu-id="ff87d-105">DESCRIPTION</span></span>
<span data-ttu-id="ff87d-106">本主題描述 Microsoft Azure PowerShell 模組的0.8.10 版本中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ff87d-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="ff87d-107">若要取得您正在使用的模組版本，請在 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。</span><span class="sxs-lookup"><span data-stu-id="ff87d-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="ff87d-108">**AzureNodeWorkerRole** Cmdlet 會建立必要的檔案和資料夾（有時稱為基架），以便透過 node.exe 在雲端中託管 Node.js 應用程式。</span><span class="sxs-lookup"><span data-stu-id="ff87d-108">The **Add-AzureNodeWorkerRole** cmdlet creates the required files and folders, sometimes referred to as scaffolding, for a Node.js application to be hosted in the cloud via node.exe.</span></span>

## <span data-ttu-id="ff87d-109">示例</span><span class="sxs-lookup"><span data-stu-id="ff87d-109">EXAMPLES</span></span>

### <span data-ttu-id="ff87d-110">範例1：單一實例 worker 角色</span><span class="sxs-lookup"><span data-stu-id="ff87d-110">Example 1: Single instance worker role</span></span>
```
PS C:\> Add-AzureWorkerRole MyWorkerRole
```

<span data-ttu-id="ff87d-111">這個範例會將一個名為 **MyWorkerRole** 的單一輔助角色角色的基架新增到目前的應用程式。</span><span class="sxs-lookup"><span data-stu-id="ff87d-111">This example adds scaffolding for a single worker role named **MyWorkerRole** to the current application.</span></span>

### <span data-ttu-id="ff87d-112">範例2：多個實例 worker 角色</span><span class="sxs-lookup"><span data-stu-id="ff87d-112">Example 2: Multiple instance worker role</span></span>
```
PS C:\> Add-AzureNodeWorkerRole MyWorkerRole -I 2
```

<span data-ttu-id="ff87d-113">這個範例會將一個名為 **MyWorkerRole** 的單一輔助角色角色的基架新增到目前的應用程式，角色實例計數為2。</span><span class="sxs-lookup"><span data-stu-id="ff87d-113">This example adds scaffolding for a single worker role named **MyWorkerRole** to the current application, with a role instance count of 2.</span></span>

## <span data-ttu-id="ff87d-114">參數</span><span class="sxs-lookup"><span data-stu-id="ff87d-114">PARAMETERS</span></span>

### <span data-ttu-id="ff87d-115">-實例</span><span class="sxs-lookup"><span data-stu-id="ff87d-115">-Instances</span></span>
<span data-ttu-id="ff87d-116">指定此 worker 角色的角色實例數。</span><span class="sxs-lookup"><span data-stu-id="ff87d-116">Specifies the number of role instances for this worker role.</span></span>
<span data-ttu-id="ff87d-117">預設值為1。</span><span class="sxs-lookup"><span data-stu-id="ff87d-117">Default is 1.</span></span>

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

### <span data-ttu-id="ff87d-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="ff87d-118">-Name</span></span>
<span data-ttu-id="ff87d-119">指定 worker 角色的名稱。</span><span class="sxs-lookup"><span data-stu-id="ff87d-119">Specifies the name of the worker role.</span></span>
<span data-ttu-id="ff87d-120">此值會決定包含在 worker 角色中主持之 node.js 服務之基架的資料夾名稱。</span><span class="sxs-lookup"><span data-stu-id="ff87d-120">The value determines the folder name that contains the scaffolding for the node.js service hosted in the worker role.</span></span>
<span data-ttu-id="ff87d-121">預設值為 WorkerRole1。</span><span class="sxs-lookup"><span data-stu-id="ff87d-121">Default is WorkerRole1.</span></span>

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

### <span data-ttu-id="ff87d-122">-設定檔</span><span class="sxs-lookup"><span data-stu-id="ff87d-122">-Profile</span></span>
<span data-ttu-id="ff87d-123">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="ff87d-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ff87d-124">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="ff87d-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ff87d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff87d-125">CommonParameters</span></span>
<span data-ttu-id="ff87d-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ff87d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff87d-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ff87d-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff87d-128">輸入</span><span class="sxs-lookup"><span data-stu-id="ff87d-128">INPUTS</span></span>

## <span data-ttu-id="ff87d-129">輸出</span><span class="sxs-lookup"><span data-stu-id="ff87d-129">OUTPUTS</span></span>

## <span data-ttu-id="ff87d-130">筆記</span><span class="sxs-lookup"><span data-stu-id="ff87d-130">NOTES</span></span>

## <span data-ttu-id="ff87d-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="ff87d-131">RELATED LINKS</span></span>

[<span data-ttu-id="ff87d-132">附加 AzureNodeWebRole</span><span class="sxs-lookup"><span data-stu-id="ff87d-132">Add-AzureNodeWebRole</span></span>](./Add-AzureNodeWebRole.md)

[<span data-ttu-id="ff87d-133">新-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="ff87d-133">New-AzureServiceProject</span></span>](./New-AzureServiceProject.md)


