---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: C2DAFB2C-A58B-406C-8349-8728771B279E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 59aef29c27d7eb96834d270c2fce48ff3acb9554
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967838"
---
# <span data-ttu-id="7a8b5-101">Add-AzureNodeWebRole</span><span class="sxs-lookup"><span data-stu-id="7a8b5-101">Add-AzureNodeWebRole</span></span>

## <span data-ttu-id="7a8b5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7a8b5-102">SYNOPSIS</span></span>
<span data-ttu-id="7a8b5-103">為 Node.js 應用程式建立必要的檔案和資料夾。</span><span class="sxs-lookup"><span data-stu-id="7a8b5-103">Creates required files and folders for a Node.js application.</span></span>

## <span data-ttu-id="7a8b5-104">句法</span><span class="sxs-lookup"><span data-stu-id="7a8b5-104">SYNTAX</span></span>

```
Add-AzureNodeWebRole [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="7a8b5-105">說明</span><span class="sxs-lookup"><span data-stu-id="7a8b5-105">DESCRIPTION</span></span>
<span data-ttu-id="7a8b5-106">本主題描述 Microsoft Azure PowerShell 模組的0.8.10 版本中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7a8b5-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="7a8b5-107">若要取得您正在使用的模組版本，請在 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。</span><span class="sxs-lookup"><span data-stu-id="7a8b5-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="7a8b5-108">**載入 AzureNodeWebRole** 會建立必要的檔案和資料夾（有時稱為基架），以供在雲端透過 IIS 託管的 Node.js 應用程式使用。</span><span class="sxs-lookup"><span data-stu-id="7a8b5-108">The **Add-AzureNodeWebRole** creates required files and folders, sometimes referred to as scaffolding, for a Node.js application to be hosted in the cloud via IIS.</span></span>

## <span data-ttu-id="7a8b5-109">示例</span><span class="sxs-lookup"><span data-stu-id="7a8b5-109">EXAMPLES</span></span>

### <span data-ttu-id="7a8b5-110">範例1：單一實例網頁角色</span><span class="sxs-lookup"><span data-stu-id="7a8b5-110">Example 1: Single instance web role</span></span>
```
PS C:\> Add-AzureNodeWebRole -Name MyWebRole
```

<span data-ttu-id="7a8b5-111">這個範例會將一個名為 **MyWebRole** 的單一網頁角色的基架新增到目前的應用程式。</span><span class="sxs-lookup"><span data-stu-id="7a8b5-111">This example adds scaffolding for a single web role named **MyWebRole** to the current application.</span></span>

### <span data-ttu-id="7a8b5-112">範例2：多重實例網頁角色</span><span class="sxs-lookup"><span data-stu-id="7a8b5-112">Example 2: Multiple instance web role</span></span>
```
PS C:\> Add-AzureNodeWebRole MyWebRole -I 2
```

<span data-ttu-id="7a8b5-113">這個範例會將一個名為 **MyWebRole** 的新網頁角色的基架新增到目前的應用程式，而角色實例計數為2。</span><span class="sxs-lookup"><span data-stu-id="7a8b5-113">This example adds scaffolding for a new web role named **MyWebRole** to the current application, with a role instance count of 2.</span></span>

## <span data-ttu-id="7a8b5-114">參數</span><span class="sxs-lookup"><span data-stu-id="7a8b5-114">PARAMETERS</span></span>

### <span data-ttu-id="7a8b5-115">-實例</span><span class="sxs-lookup"><span data-stu-id="7a8b5-115">-Instances</span></span>
<span data-ttu-id="7a8b5-116">指定此網頁角色的角色實例數。</span><span class="sxs-lookup"><span data-stu-id="7a8b5-116">Specifies the number of role instances for this web role.</span></span>
<span data-ttu-id="7a8b5-117">預設值為1。</span><span class="sxs-lookup"><span data-stu-id="7a8b5-117">The default is 1.</span></span>

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

### <span data-ttu-id="7a8b5-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="7a8b5-118">-Name</span></span>
<span data-ttu-id="7a8b5-119">指定網頁角色的名稱。</span><span class="sxs-lookup"><span data-stu-id="7a8b5-119">Specifies the name of the web role.</span></span>
<span data-ttu-id="7a8b5-120">它也會決定包含要以網頁角色託管之 node.js 應用程式的基架的目錄名稱。</span><span class="sxs-lookup"><span data-stu-id="7a8b5-120">It also determines the name of the directory that contains the scaffolding for the node.js application that will be hosted in the web role.</span></span>
<span data-ttu-id="7a8b5-121">預設值為 WebRole #，其中 # 代表服務中的網頁角色數目。</span><span class="sxs-lookup"><span data-stu-id="7a8b5-121">The default is WebRole#, where # indicates the number of web roles in the service.</span></span>

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

### <span data-ttu-id="7a8b5-122">-設定檔</span><span class="sxs-lookup"><span data-stu-id="7a8b5-122">-Profile</span></span>
<span data-ttu-id="7a8b5-123">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="7a8b5-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7a8b5-124">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="7a8b5-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7a8b5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a8b5-125">CommonParameters</span></span>
<span data-ttu-id="7a8b5-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7a8b5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a8b5-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7a8b5-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a8b5-128">輸入</span><span class="sxs-lookup"><span data-stu-id="7a8b5-128">INPUTS</span></span>

## <span data-ttu-id="7a8b5-129">輸出</span><span class="sxs-lookup"><span data-stu-id="7a8b5-129">OUTPUTS</span></span>

## <span data-ttu-id="7a8b5-130">筆記</span><span class="sxs-lookup"><span data-stu-id="7a8b5-130">NOTES</span></span>

## <span data-ttu-id="7a8b5-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="7a8b5-131">RELATED LINKS</span></span>

[<span data-ttu-id="7a8b5-132">附加 AzureNodeWorkerRole</span><span class="sxs-lookup"><span data-stu-id="7a8b5-132">Add-AzureNodeWorkerRole</span></span>](./Add-AzureNodeWorkerRole.md)

[<span data-ttu-id="7a8b5-133">新-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="7a8b5-133">New-AzureServiceProject</span></span>](./New-AzureServiceProject.md)


