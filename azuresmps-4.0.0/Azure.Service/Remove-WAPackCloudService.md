---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 1ECF6BB5-3751-4DA0-AC6C-A64F15F46D26
online version: ''
schema: 2.0.0
ms.openlocfilehash: 552c2511a806abb4329860e7c15d8a68b5e03f79
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/08/2020
ms.locfileid: "93968859"
---
# <span data-ttu-id="8ee47-101">Remove-WAPackCloudService</span><span class="sxs-lookup"><span data-stu-id="8ee47-101">Remove-WAPackCloudService</span></span>

## <span data-ttu-id="8ee47-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8ee47-102">SYNOPSIS</span></span>
<span data-ttu-id="8ee47-103">移除雲端服務物件。</span><span class="sxs-lookup"><span data-stu-id="8ee47-103">Removes cloud service objects.</span></span>

## <span data-ttu-id="8ee47-104">句法</span><span class="sxs-lookup"><span data-stu-id="8ee47-104">SYNTAX</span></span>

```
Remove-WAPackCloudService -CloudService <CloudService> [-PassThru] [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ee47-105">說明</span><span class="sxs-lookup"><span data-stu-id="8ee47-105">DESCRIPTION</span></span>
<span data-ttu-id="8ee47-106">這些主題已棄用，未來將會移除。</span><span class="sxs-lookup"><span data-stu-id="8ee47-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="8ee47-107">本主題描述 Microsoft Azure PowerShell 模組的0.8.1 版本中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8ee47-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="8ee47-108">若要找出您正在使用的模組版本，請從 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。</span><span class="sxs-lookup"><span data-stu-id="8ee47-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="8ee47-109">**WAPackCloudService** Cmdlet 會移除雲端服務物件。</span><span class="sxs-lookup"><span data-stu-id="8ee47-109">The **Remove-WAPackCloudService** cmdlet removes cloud service objects.</span></span>

## <span data-ttu-id="8ee47-110">示例</span><span class="sxs-lookup"><span data-stu-id="8ee47-110">EXAMPLES</span></span>

### <span data-ttu-id="8ee47-111">範例1：移除雲端服務</span><span class="sxs-lookup"><span data-stu-id="8ee47-111">Example 1: Remove a cloud service</span></span>
```
PS C:\> $CloudService = Get-WAPackCloudService -Name "ContosoCloudService01"
PS C:\> Remove-WAPackVM -VM $CloudService
```

<span data-ttu-id="8ee47-112">第一個命令會使用 **WAPackCloudService** Cmdlet 取得名為 ContosoCloudService01 的雲端服務，然後將該物件儲存在 $CloudService 變數中。</span><span class="sxs-lookup"><span data-stu-id="8ee47-112">The first command gets the cloud service named ContosoCloudService01 by using the **Get-WAPackCloudService** cmdlet, and then stores that object in the $CloudService variable.</span></span>

<span data-ttu-id="8ee47-113">第二個命令會移除 $CloudService 中儲存的 cloudservice。</span><span class="sxs-lookup"><span data-stu-id="8ee47-113">The second command removes the cloudservice stored in $CloudService.</span></span>
<span data-ttu-id="8ee47-114">命令會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8ee47-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="8ee47-115">範例2：移除雲端服務而不進行確認</span><span class="sxs-lookup"><span data-stu-id="8ee47-115">Example 2: Remove a cloud service without confirmation</span></span>
```
PS C:\> $CloudService = Get-WAPackCloudService -Name "ContosoCloudService02"
PS C:\> Remove-WAPackCloudService -VM $CloudService -Force
```

<span data-ttu-id="8ee47-116">第一個命令會使用 **WAPackCloudService** Cmdlet 取得名為 ContosoCloudService02 的雲端服務，然後將該物件儲存在 $CloudService 變數中。</span><span class="sxs-lookup"><span data-stu-id="8ee47-116">The first command gets the cloud service named ContosoCloudService02 by using the **Get-WAPackCloudService** cmdlet, and then stores that object in the $CloudService variable.</span></span>

<span data-ttu-id="8ee47-117">第二個命令會移除 $CloudService 中儲存的雲端服務。</span><span class="sxs-lookup"><span data-stu-id="8ee47-117">The second command removes the cloud service stored in $CloudService.</span></span>
<span data-ttu-id="8ee47-118">這個命令包含 *Force* 參數。</span><span class="sxs-lookup"><span data-stu-id="8ee47-118">This command includes the *Force* parameter.</span></span>
<span data-ttu-id="8ee47-119">該命令不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8ee47-119">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="8ee47-120">參數</span><span class="sxs-lookup"><span data-stu-id="8ee47-120">PARAMETERS</span></span>

### <span data-ttu-id="8ee47-121">-CloudService</span><span class="sxs-lookup"><span data-stu-id="8ee47-121">-CloudService</span></span>
<span data-ttu-id="8ee47-122">指定雲端服務物件。</span><span class="sxs-lookup"><span data-stu-id="8ee47-122">Specifies a cloud service object.</span></span>
<span data-ttu-id="8ee47-123">若要取得雲端服務，請使用 **WAPackCloudService** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8ee47-123">To obtain a cloud service, use the **Get-WAPackCloudService** cmdlet.</span></span>

```yaml
Type: CloudService
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8ee47-124">-Force</span><span class="sxs-lookup"><span data-stu-id="8ee47-124">-Force</span></span>
<span data-ttu-id="8ee47-125">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="8ee47-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8ee47-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8ee47-126">-PassThru</span></span>
<span data-ttu-id="8ee47-127">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="8ee47-127">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="8ee47-128">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="8ee47-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8ee47-129">-設定檔</span><span class="sxs-lookup"><span data-stu-id="8ee47-129">-Profile</span></span>
<span data-ttu-id="8ee47-130">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="8ee47-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8ee47-131">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="8ee47-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8ee47-132">-確認</span><span class="sxs-lookup"><span data-stu-id="8ee47-132">-Confirm</span></span>
<span data-ttu-id="8ee47-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8ee47-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ee47-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ee47-134">-WhatIf</span></span>
<span data-ttu-id="8ee47-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8ee47-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ee47-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8ee47-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ee47-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ee47-137">CommonParameters</span></span>
<span data-ttu-id="8ee47-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8ee47-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ee47-139">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8ee47-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ee47-140">輸入</span><span class="sxs-lookup"><span data-stu-id="8ee47-140">INPUTS</span></span>

## <span data-ttu-id="8ee47-141">輸出</span><span class="sxs-lookup"><span data-stu-id="8ee47-141">OUTPUTS</span></span>

## <span data-ttu-id="8ee47-142">筆記</span><span class="sxs-lookup"><span data-stu-id="8ee47-142">NOTES</span></span>

## <span data-ttu-id="8ee47-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="8ee47-143">RELATED LINKS</span></span>

[<span data-ttu-id="8ee47-144">WAPackCloudService</span><span class="sxs-lookup"><span data-stu-id="8ee47-144">Get-WAPackCloudService</span></span>](./Get-WAPackCloudService.md)

[<span data-ttu-id="8ee47-145">新-WAPackCloudService</span><span class="sxs-lookup"><span data-stu-id="8ee47-145">New-WAPackCloudService</span></span>](./New-WAPackCloudService.md)


