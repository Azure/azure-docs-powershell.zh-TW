---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 8632A865-D4CC-4AE5-8307-055CDD776D26
online version: ''
schema: 2.0.0
ms.openlocfilehash: a2b79ee50bb5097896c2a120a9b7316adb2146b5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967156"
---
# <span data-ttu-id="14da8-101">Add-AzureWorkerRole</span><span class="sxs-lookup"><span data-stu-id="14da8-101">Add-AzureWorkerRole</span></span>

## <span data-ttu-id="14da8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="14da8-102">SYNOPSIS</span></span>
<span data-ttu-id="14da8-103">建立自訂工作人員角色所需的檔案和配置。</span><span class="sxs-lookup"><span data-stu-id="14da8-103">Creates required files and configuration for a custom worker role.</span></span>

## <span data-ttu-id="14da8-104">句法</span><span class="sxs-lookup"><span data-stu-id="14da8-104">SYNTAX</span></span>

```
Add-AzureWorkerRole [-TemplateFolder <String>] [-Name <String>] [-Instances <Int32>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="14da8-105">說明</span><span class="sxs-lookup"><span data-stu-id="14da8-105">DESCRIPTION</span></span>
<span data-ttu-id="14da8-106">本主題描述 Microsoft Azure PowerShell 模組的0.8.10 版本中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="14da8-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="14da8-107">若要取得您正在使用的模組版本，請在 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。</span><span class="sxs-lookup"><span data-stu-id="14da8-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="14da8-108">**AzureWorkerRole** Cmdlet 會針對自訂輔助角色建立必要的檔案和設定（有時稱為基架）。</span><span class="sxs-lookup"><span data-stu-id="14da8-108">The **Add-AzureWorkerRole** cmdlet creates required files and configuration, sometimes referred to as scaffolding, for a custom worker role.</span></span>

## <span data-ttu-id="14da8-109">示例</span><span class="sxs-lookup"><span data-stu-id="14da8-109">EXAMPLES</span></span>

### <span data-ttu-id="14da8-110">範例1：建立單一實例 worker 角色</span><span class="sxs-lookup"><span data-stu-id="14da8-110">Example 1: Create a single instance worker role</span></span>
```
PS C:\> Add-AzureWorkerRole -Name MyWorkerRole
```

<span data-ttu-id="14da8-111">這個範例會將一個名為 MyWorkerRole 的單一輔助角色角色的基架新增到目前的應用程式。</span><span class="sxs-lookup"><span data-stu-id="14da8-111">This example adds scaffolding for a single worker role named MyWorkerRole to the current application.</span></span>

### <span data-ttu-id="14da8-112">範例2：建立多個實例 worker 角色</span><span class="sxs-lookup"><span data-stu-id="14da8-112">Example 2: Create a multiple instance worker role</span></span>
```
PS C:\> Add-AzureWorkerRole MyWorkerRole -I 2
```

<span data-ttu-id="14da8-113">這個範例會將一個名為 MyWorkerRole 的新輔助角色角色的基架新增到目前的應用程式，而角色實例計數為2。</span><span class="sxs-lookup"><span data-stu-id="14da8-113">This example adds scaffolding for a new worker role named MyWorkerRole to the current application, with a role instance count of 2.</span></span>

### <span data-ttu-id="14da8-114">範例3：建立含自訂基架的 worker 角色</span><span class="sxs-lookup"><span data-stu-id="14da8-114">Example 3: Create worker role with custom scaffolding</span></span>
```
PS C:\> Add-AzureWorkerRole MyWorkerRole -TemplateFoldr .\MyWorkerRoleTemplate
```

<span data-ttu-id="14da8-115">這個範例會建立含自訂基架的 worker 角色。</span><span class="sxs-lookup"><span data-stu-id="14da8-115">This example creates a worker role with custom scaffolding.</span></span>

## <span data-ttu-id="14da8-116">參數</span><span class="sxs-lookup"><span data-stu-id="14da8-116">PARAMETERS</span></span>

### <span data-ttu-id="14da8-117">-實例</span><span class="sxs-lookup"><span data-stu-id="14da8-117">-Instances</span></span>
<span data-ttu-id="14da8-118">指定此 worker 角色的角色實例數。</span><span class="sxs-lookup"><span data-stu-id="14da8-118">Specifies the number of role instances for this worker role.</span></span>
<span data-ttu-id="14da8-119">預設值為1。</span><span class="sxs-lookup"><span data-stu-id="14da8-119">The default is 1.</span></span>

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

### <span data-ttu-id="14da8-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="14da8-120">-Name</span></span>
<span data-ttu-id="14da8-121">指定 worker 角色的名稱。</span><span class="sxs-lookup"><span data-stu-id="14da8-121">Specifies the name of the worker role.</span></span>
<span data-ttu-id="14da8-122">這個值會決定包含自訂應用程式的基架的資料夾名稱，這些基架將寄宿在輔助角色中。</span><span class="sxs-lookup"><span data-stu-id="14da8-122">This value determines the folder name that contains the scaffolding for the custom application that will be hosted in the worker role.</span></span>
<span data-ttu-id="14da8-123">預設值為 WorkerRolenumber，其中 number 是服務中輔助角色的數目。</span><span class="sxs-lookup"><span data-stu-id="14da8-123">The default is WorkerRolenumber, where number is the number of worker roles in the service.</span></span>

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

### <span data-ttu-id="14da8-124">-設定檔</span><span class="sxs-lookup"><span data-stu-id="14da8-124">-Profile</span></span>
<span data-ttu-id="14da8-125">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="14da8-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="14da8-126">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="14da8-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="14da8-127">-TemplateFolder</span><span class="sxs-lookup"><span data-stu-id="14da8-127">-TemplateFolder</span></span>
<span data-ttu-id="14da8-128">指定要用來建立 worker 角色的 [基架範本] 資料夾。</span><span class="sxs-lookup"><span data-stu-id="14da8-128">Specifies the scaffolding template folder to be used to create the worker role.</span></span>

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

### <span data-ttu-id="14da8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14da8-129">CommonParameters</span></span>
<span data-ttu-id="14da8-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="14da8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14da8-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="14da8-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14da8-132">輸入</span><span class="sxs-lookup"><span data-stu-id="14da8-132">INPUTS</span></span>

## <span data-ttu-id="14da8-133">輸出</span><span class="sxs-lookup"><span data-stu-id="14da8-133">OUTPUTS</span></span>

## <span data-ttu-id="14da8-134">筆記</span><span class="sxs-lookup"><span data-stu-id="14da8-134">NOTES</span></span>

## <span data-ttu-id="14da8-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="14da8-135">RELATED LINKS</span></span>

[<span data-ttu-id="14da8-136">附加 AzureWebRole</span><span class="sxs-lookup"><span data-stu-id="14da8-136">Add-AzureWebRole</span></span>](./Add-AzureWebRole.md)

[<span data-ttu-id="14da8-137">新-AzureRoleTemplate</span><span class="sxs-lookup"><span data-stu-id="14da8-137">New-AzureRoleTemplate</span></span>](./New-AzureRoleTemplate.md)


