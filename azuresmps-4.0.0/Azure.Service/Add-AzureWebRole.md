---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: FB5CD696-108D-4A3E-8983-1C6562E8795A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 25ade8ccf395d37ab0856742fe473a6508c9d63b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967157"
---
# <span data-ttu-id="b02e8-101">Add-AzureWebRole</span><span class="sxs-lookup"><span data-stu-id="b02e8-101">Add-AzureWebRole</span></span>

## <span data-ttu-id="b02e8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b02e8-102">SYNOPSIS</span></span>
<span data-ttu-id="b02e8-103">新增 web worker 角色。</span><span class="sxs-lookup"><span data-stu-id="b02e8-103">Adds a web worker role.</span></span>

## <span data-ttu-id="b02e8-104">句法</span><span class="sxs-lookup"><span data-stu-id="b02e8-104">SYNTAX</span></span>

```
Add-AzureWebRole [-TemplateFolder <String>] [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="b02e8-105">說明</span><span class="sxs-lookup"><span data-stu-id="b02e8-105">DESCRIPTION</span></span>
<span data-ttu-id="b02e8-106">本主題描述 Microsoft Azure PowerShell 模組的0.8.10 版本中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b02e8-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="b02e8-107">若要取得您正在使用的模組版本，請在 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。</span><span class="sxs-lookup"><span data-stu-id="b02e8-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="b02e8-108">**AzureWebRole** Cmdlet 會新增 web worker 角色。</span><span class="sxs-lookup"><span data-stu-id="b02e8-108">The **Add-AzureWebRole** cmdlet adds a web worker role.</span></span>

## <span data-ttu-id="b02e8-109">示例</span><span class="sxs-lookup"><span data-stu-id="b02e8-109">EXAMPLES</span></span>

### <span data-ttu-id="b02e8-110">範例1：新增預設角色</span><span class="sxs-lookup"><span data-stu-id="b02e8-110">Example 1: Add a default role</span></span>
```
PS C:\> Add-AzureWebRole
```

<span data-ttu-id="b02e8-111">這個命令會新增網頁角色，此角色的預設設定為 Webrole1 名稱與單一實例。</span><span class="sxs-lookup"><span data-stu-id="b02e8-111">This command add web role that has the default configuration of Webrole1 as the name and a single instance.</span></span>

### <span data-ttu-id="b02e8-112">範例2：新增具有名稱的角色</span><span class="sxs-lookup"><span data-stu-id="b02e8-112">Example 2: Add a role with a name</span></span>
```
PS C:\> Add-AzureWebRole -Name "MyWebRole"
```

<span data-ttu-id="b02e8-113">這個命令會將一個名為 MyWebRole 的單一網頁角色新增至目前的應用程式。</span><span class="sxs-lookup"><span data-stu-id="b02e8-113">This command adds a single web role named MyWebRole to the current application.</span></span>

### <span data-ttu-id="b02e8-114">範例3：新增具有名稱和實例計數的角色</span><span class="sxs-lookup"><span data-stu-id="b02e8-114">Example 3: Add a role with a name and instance count</span></span>
```
PS C:\> Add-AzureWebRole -Name "MyWebRole" -Instance 2
```

<span data-ttu-id="b02e8-115">這個命令會將名為 MyWebRole 的網站角色新增至目前的應用程式。</span><span class="sxs-lookup"><span data-stu-id="b02e8-115">This command adds a web role named MyWebRole to the current application.</span></span>
<span data-ttu-id="b02e8-116">Cmdlet 的角色實例計數為2。</span><span class="sxs-lookup"><span data-stu-id="b02e8-116">The cmdlet has a role instance count of 2.</span></span>

### <span data-ttu-id="b02e8-117">範例4：新增具有名稱和範本的角色</span><span class="sxs-lookup"><span data-stu-id="b02e8-117">Example 4: Add a role with a name and template</span></span>
```
PS C:\> Add-AzureWebRole -Name "MyWebRole" -TemplateFolder ".\MyWebTemplateFolder"
```

<span data-ttu-id="b02e8-118">這個命令會將一個名為 MyWebRole 的單一網頁角色新增至目前的應用程式。</span><span class="sxs-lookup"><span data-stu-id="b02e8-118">This command adds a single web role named MyWebRole to the current application.</span></span>
<span data-ttu-id="b02e8-119">該命令會將名為 MyWebTemplateFolder 的資料夾指定為基架範本。</span><span class="sxs-lookup"><span data-stu-id="b02e8-119">The command specifies a folder named MyWebTemplateFolder as a scaffolding template.</span></span>

## <span data-ttu-id="b02e8-120">參數</span><span class="sxs-lookup"><span data-stu-id="b02e8-120">PARAMETERS</span></span>

### <span data-ttu-id="b02e8-121">-實例</span><span class="sxs-lookup"><span data-stu-id="b02e8-121">-Instances</span></span>
<span data-ttu-id="b02e8-122">指定實例數。</span><span class="sxs-lookup"><span data-stu-id="b02e8-122">Specifies the number of instances.</span></span>

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

### <span data-ttu-id="b02e8-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="b02e8-123">-Name</span></span>
<span data-ttu-id="b02e8-124">指定網頁角色的名稱。</span><span class="sxs-lookup"><span data-stu-id="b02e8-124">Specifies the name of the web role.</span></span>

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

### <span data-ttu-id="b02e8-125">-設定檔</span><span class="sxs-lookup"><span data-stu-id="b02e8-125">-Profile</span></span>
<span data-ttu-id="b02e8-126">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="b02e8-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b02e8-127">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="b02e8-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b02e8-128">-TemplateFolder</span><span class="sxs-lookup"><span data-stu-id="b02e8-128">-TemplateFolder</span></span>
<span data-ttu-id="b02e8-129">指定 [範本] 資料夾。</span><span class="sxs-lookup"><span data-stu-id="b02e8-129">Specifies the template folder.</span></span>

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

### <span data-ttu-id="b02e8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b02e8-130">CommonParameters</span></span>
<span data-ttu-id="b02e8-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b02e8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b02e8-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b02e8-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b02e8-133">輸入</span><span class="sxs-lookup"><span data-stu-id="b02e8-133">INPUTS</span></span>

## <span data-ttu-id="b02e8-134">輸出</span><span class="sxs-lookup"><span data-stu-id="b02e8-134">OUTPUTS</span></span>

## <span data-ttu-id="b02e8-135">筆記</span><span class="sxs-lookup"><span data-stu-id="b02e8-135">NOTES</span></span>

## <span data-ttu-id="b02e8-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="b02e8-136">RELATED LINKS</span></span>

[<span data-ttu-id="b02e8-137">附加 AzureWorkerRole</span><span class="sxs-lookup"><span data-stu-id="b02e8-137">Add-AzureWorkerRole</span></span>](./Add-AzureWorkerRole.md)

[<span data-ttu-id="b02e8-138">新-AzureRoleTemplate</span><span class="sxs-lookup"><span data-stu-id="b02e8-138">New-AzureRoleTemplate</span></span>](./New-AzureRoleTemplate.md)


