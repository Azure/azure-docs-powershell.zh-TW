---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 5D093C10-F8B6-4F4A-ABD7-CC4D7AB7AFFA
online version: ''
schema: 2.0.0
ms.openlocfilehash: c78f53b95d18de600535368a1109b318294928c3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967398"
---
# <span data-ttu-id="51567-101">Set-AzureServiceProjectRole</span><span class="sxs-lookup"><span data-stu-id="51567-101">Set-AzureServiceProjectRole</span></span>

## <span data-ttu-id="51567-102">摘要</span><span class="sxs-lookup"><span data-stu-id="51567-102">SYNOPSIS</span></span>
<span data-ttu-id="51567-103">設定角色的實例數或執行時間版本。</span><span class="sxs-lookup"><span data-stu-id="51567-103">Sets the number of instances or the runtime version of a role.</span></span>

## <span data-ttu-id="51567-104">句法</span><span class="sxs-lookup"><span data-stu-id="51567-104">SYNTAX</span></span>

### <span data-ttu-id="51567-105">範例</span><span class="sxs-lookup"><span data-stu-id="51567-105">Instances</span></span>
```
Set-AzureServiceProjectRole [-RoleName <String>] -Instances <Int32> [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="51567-106">時時</span><span class="sxs-lookup"><span data-stu-id="51567-106">Runtime</span></span>
```
Set-AzureServiceProjectRole [-RoleName <String>] -Runtime <String> -Version <String> [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="51567-107">VMSize</span><span class="sxs-lookup"><span data-stu-id="51567-107">VMSize</span></span>
```
Set-AzureServiceProjectRole [-RoleName <String>] [-PassThru] -VMSize <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="51567-108">說明</span><span class="sxs-lookup"><span data-stu-id="51567-108">DESCRIPTION</span></span>
<span data-ttu-id="51567-109">本主題描述 Microsoft Azure PowerShell 模組的0.8.10 版本中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="51567-109">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="51567-110">若要取得您正在使用的模組版本，請在 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。</span><span class="sxs-lookup"><span data-stu-id="51567-110">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="51567-111">**AzureServiceProjectRole** Cmdlet 會設定指定角色的角色實例數。</span><span class="sxs-lookup"><span data-stu-id="51567-111">The **Set-AzureServiceProjectRole** cmdlet sets the number of role instances for the specified role.</span></span>

## <span data-ttu-id="51567-112">示例</span><span class="sxs-lookup"><span data-stu-id="51567-112">EXAMPLES</span></span>

### <span data-ttu-id="51567-113">範例1：設定網頁角色的實例</span><span class="sxs-lookup"><span data-stu-id="51567-113">Example 1: Set instances for a web role</span></span>
```
PS C:\> Set-AzureServiceProjectRole "MyWebRole" 2
```

<span data-ttu-id="51567-114">將名為 MyWebRole1 的網頁角色的實例數設定為2。</span><span class="sxs-lookup"><span data-stu-id="51567-114">Sets the number of instances for the web role named MyWebRole1 to 2.</span></span>

### <span data-ttu-id="51567-115">範例2：設定 worker 角色的實例</span><span class="sxs-lookup"><span data-stu-id="51567-115">Example 2: Set instances for a worker role</span></span>
```
PS C:\> Set-AzureServiceProjectRole "MyWorkerRole1" 2
```

<span data-ttu-id="51567-116">將名為 WorkerRole1 的 worker 角色的角色實例計數設定為2。</span><span class="sxs-lookup"><span data-stu-id="51567-116">Sets the role instance count for the worker role named WorkerRole1 to 2.</span></span>

### <span data-ttu-id="51567-117">範例3：設定角色服務的執行時間版本</span><span class="sxs-lookup"><span data-stu-id="51567-117">Example 3: Set the runtime version for a role service</span></span>
```
PS C:\> Set-AzureServiceProjectRole "MyRole1" node 0.6.20
```

<span data-ttu-id="51567-118">將角色 MyRole1 的 node.exe 執行時間版本設定為0.6.20。</span><span class="sxs-lookup"><span data-stu-id="51567-118">Sets the node.exe runtime version for role MyRole1 to 0.6.20.</span></span>

## <span data-ttu-id="51567-119">參數</span><span class="sxs-lookup"><span data-stu-id="51567-119">PARAMETERS</span></span>

### <span data-ttu-id="51567-120">-實例</span><span class="sxs-lookup"><span data-stu-id="51567-120">-Instances</span></span>
<span data-ttu-id="51567-121">指定指定網站或 worker 角色的角色實例數。</span><span class="sxs-lookup"><span data-stu-id="51567-121">Specifies the number of role instances for the specified web or worker role.</span></span>

```yaml
Type: Int32
Parameter Sets: Instances
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51567-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="51567-122">-PassThru</span></span>
<span data-ttu-id="51567-123">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="51567-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="51567-124">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="51567-124">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51567-125">-設定檔</span><span class="sxs-lookup"><span data-stu-id="51567-125">-Profile</span></span>
<span data-ttu-id="51567-126">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="51567-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="51567-127">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="51567-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="51567-128">-擁有方</span><span class="sxs-lookup"><span data-stu-id="51567-128">-RoleName</span></span>
<span data-ttu-id="51567-129">指定要變更的網站名稱或 worker 角色。</span><span class="sxs-lookup"><span data-stu-id="51567-129">Specifies the name of the web or worker role to be changed.</span></span>

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

### <span data-ttu-id="51567-130">-執行時間</span><span class="sxs-lookup"><span data-stu-id="51567-130">-Runtime</span></span>
<span data-ttu-id="51567-131">指定要新增至指定角色的執行時間。</span><span class="sxs-lookup"><span data-stu-id="51567-131">Specifies the runtime to add to the specified role.</span></span>

```yaml
Type: String
Parameter Sets: Runtime
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51567-132">-版本</span><span class="sxs-lookup"><span data-stu-id="51567-132">-Version</span></span>
<span data-ttu-id="51567-133">指定要新增至角色的執行時間版本。</span><span class="sxs-lookup"><span data-stu-id="51567-133">Specifies the version of the runtime to add to the role.</span></span>

```yaml
Type: String
Parameter Sets: Runtime
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51567-134">-VMSize</span><span class="sxs-lookup"><span data-stu-id="51567-134">-VMSize</span></span>
<span data-ttu-id="51567-135">指定角色的虛擬機器大小。</span><span class="sxs-lookup"><span data-stu-id="51567-135">Specifies the virtual machine size of the role.</span></span>

```yaml
Type: String
Parameter Sets: VMSize
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51567-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51567-136">CommonParameters</span></span>
<span data-ttu-id="51567-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="51567-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51567-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="51567-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51567-139">輸入</span><span class="sxs-lookup"><span data-stu-id="51567-139">INPUTS</span></span>

###  
<span data-ttu-id="51567-140">指定虛擬機器的大小。</span><span class="sxs-lookup"><span data-stu-id="51567-140">Specifies the size of the virtual machine.</span></span>

## <span data-ttu-id="51567-141">輸出</span><span class="sxs-lookup"><span data-stu-id="51567-141">OUTPUTS</span></span>

## <span data-ttu-id="51567-142">筆記</span><span class="sxs-lookup"><span data-stu-id="51567-142">NOTES</span></span>

## <span data-ttu-id="51567-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="51567-143">RELATED LINKS</span></span>

[<span data-ttu-id="51567-144">Set-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="51567-144">Set-AzureServiceProject</span></span>](./Set-AzureServiceProject.md)


