---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: F9A06B8B-55DB-48A5-B246-53347E759E64
online version: ''
schema: 2.0.0
ms.openlocfilehash: 050c05f2cdad546388744bcebca4f28a12a03038
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967836"
---
# <span data-ttu-id="12e71-101">Add-AzurePHPWebRole</span><span class="sxs-lookup"><span data-stu-id="12e71-101">Add-AzurePHPWebRole</span></span>

## <span data-ttu-id="12e71-102">摘要</span><span class="sxs-lookup"><span data-stu-id="12e71-102">SYNOPSIS</span></span>
<span data-ttu-id="12e71-103">建立 PHP 應用程式所需的檔案和配置。</span><span class="sxs-lookup"><span data-stu-id="12e71-103">Creates the required files and configuration for a PHP application.</span></span>

## <span data-ttu-id="12e71-104">句法</span><span class="sxs-lookup"><span data-stu-id="12e71-104">SYNTAX</span></span>

```
Add-AzurePHPWebRole [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="12e71-105">說明</span><span class="sxs-lookup"><span data-stu-id="12e71-105">DESCRIPTION</span></span>
<span data-ttu-id="12e71-106">本主題描述 Microsoft Azure PowerShell 模組的0.8.10 版本中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="12e71-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="12e71-107">若要取得您正在使用的模組版本，請在 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。</span><span class="sxs-lookup"><span data-stu-id="12e71-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="12e71-108">**AzurePHPWebRole** Cmdlet 會針對將透過 IIS 託管在 Azure 中的 PHP 應用程式，建立檔案和設定（有時稱為基架）。</span><span class="sxs-lookup"><span data-stu-id="12e71-108">The **Add-AzurePHPWebRole** cmdlet creates the files and configuration, sometimes referred to as scaffolding, for a PHP application that will be hosted in Azure through IIS.</span></span>

## <span data-ttu-id="12e71-109">示例</span><span class="sxs-lookup"><span data-stu-id="12e71-109">EXAMPLES</span></span>

### <span data-ttu-id="12e71-110">範例1：使用預設值新增網頁角色</span><span class="sxs-lookup"><span data-stu-id="12e71-110">Example 1: Add a web role using default values</span></span>
```
PS C:\> Add-AzurePHPWebRole
```

<span data-ttu-id="12e71-111">這個範例會使用一個名為 "WebRole1" 的服務的預設值，為新的網頁角色新增所需的檔案和配置，其中包含1個實例。</span><span class="sxs-lookup"><span data-stu-id="12e71-111">This example adds the required files and configuration for new web role using the default values of a service named "WebRole1" with 1 instance.</span></span>

### <span data-ttu-id="12e71-112">範例2：新增具有多個實例的網頁角色</span><span class="sxs-lookup"><span data-stu-id="12e71-112">Example 2: Add a web role with multiple instances</span></span>
```
PS C:\> Add-AzurePHPWebRole MyWebRole -I 2
```

<span data-ttu-id="12e71-113">這個範例會將新網頁角色所需的檔案和配置，新增至目前的應用程式，並使用名稱 "MyWebRole" 和角色實例計數2。</span><span class="sxs-lookup"><span data-stu-id="12e71-113">This example adds the required files and configuration for a new web role to the current application, using the name "MyWebRole" and a role instance count of 2.</span></span>

## <span data-ttu-id="12e71-114">參數</span><span class="sxs-lookup"><span data-stu-id="12e71-114">PARAMETERS</span></span>

### <span data-ttu-id="12e71-115">-實例</span><span class="sxs-lookup"><span data-stu-id="12e71-115">-Instances</span></span>
<span data-ttu-id="12e71-116">指定此網頁角色的角色實例數。</span><span class="sxs-lookup"><span data-stu-id="12e71-116">Specifies the number of role instances for this web role.</span></span>
<span data-ttu-id="12e71-117">預設值為1。</span><span class="sxs-lookup"><span data-stu-id="12e71-117">The default is 1.</span></span>

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

### <span data-ttu-id="12e71-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="12e71-118">-Name</span></span>
<span data-ttu-id="12e71-119">指定網頁角色的名稱。</span><span class="sxs-lookup"><span data-stu-id="12e71-119">Specifies the name of the web role.</span></span>
<span data-ttu-id="12e71-120">名稱會決定包含 PHP 應用程式所需檔案和配置的目錄名稱。</span><span class="sxs-lookup"><span data-stu-id="12e71-120">The name determines the name of the directory that contains the required files and configuration for the PHP application.</span></span>
<span data-ttu-id="12e71-121">預設值為 WebRole #，其中 # 是服務中網頁角色的數目。</span><span class="sxs-lookup"><span data-stu-id="12e71-121">The default is WebRole#, where # is the number of web roles in the service.</span></span>

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

### <span data-ttu-id="12e71-122">-設定檔</span><span class="sxs-lookup"><span data-stu-id="12e71-122">-Profile</span></span>
<span data-ttu-id="12e71-123">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="12e71-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="12e71-124">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="12e71-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="12e71-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12e71-125">CommonParameters</span></span>
<span data-ttu-id="12e71-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="12e71-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12e71-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="12e71-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12e71-128">輸入</span><span class="sxs-lookup"><span data-stu-id="12e71-128">INPUTS</span></span>

## <span data-ttu-id="12e71-129">輸出</span><span class="sxs-lookup"><span data-stu-id="12e71-129">OUTPUTS</span></span>

## <span data-ttu-id="12e71-130">筆記</span><span class="sxs-lookup"><span data-stu-id="12e71-130">NOTES</span></span>

## <span data-ttu-id="12e71-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="12e71-131">RELATED LINKS</span></span>

[<span data-ttu-id="12e71-132">附加 AzurePHPWorkerRole</span><span class="sxs-lookup"><span data-stu-id="12e71-132">Add-AzurePHPWorkerRole</span></span>](./Add-AzurePHPWorkerRole.md)

[<span data-ttu-id="12e71-133">新-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="12e71-133">New-AzureServiceProject</span></span>](./New-AzureServiceProject.md)


