---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 9999E0EE-4A32-4C18-A6EC-2A073DC08710
online version: ''
schema: 2.0.0
ms.openlocfilehash: e5dfe0f42987ba51613ff9bafa000713456dfaf7
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/08/2020
ms.locfileid: "93968857"
---
# <span data-ttu-id="4bf22-101">Remove-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="4bf22-101">Remove-WAPackVMRole</span></span>

## <span data-ttu-id="4bf22-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4bf22-102">SYNOPSIS</span></span>
<span data-ttu-id="4bf22-103">移除虛擬機器角色物件。</span><span class="sxs-lookup"><span data-stu-id="4bf22-103">Removes virtual machine role objects.</span></span>

## <span data-ttu-id="4bf22-104">句法</span><span class="sxs-lookup"><span data-stu-id="4bf22-104">SYNTAX</span></span>

### <span data-ttu-id="4bf22-105">FromVMRoleObject (預設) </span><span class="sxs-lookup"><span data-stu-id="4bf22-105">FromVMRoleObject (Default)</span></span>
```
Remove-WAPackVMRole -VMRole <VMRole> [-PassThru] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4bf22-106">FromCloudService</span><span class="sxs-lookup"><span data-stu-id="4bf22-106">FromCloudService</span></span>
```
Remove-WAPackVMRole -VMRole <VMRole> -CloudServiceName <String> [-PassThru] [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4bf22-107">說明</span><span class="sxs-lookup"><span data-stu-id="4bf22-107">DESCRIPTION</span></span>
<span data-ttu-id="4bf22-108">這些主題已棄用，未來將會移除。</span><span class="sxs-lookup"><span data-stu-id="4bf22-108">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="4bf22-109">本主題描述 Microsoft Azure PowerShell 模組的0.8.1 版本中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4bf22-109">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="4bf22-110">若要找出您正在使用的模組版本，請從 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。</span><span class="sxs-lookup"><span data-stu-id="4bf22-110">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="4bf22-111">**WAPackVMRole** Cmdlet 會移除虛擬機器角色物件。</span><span class="sxs-lookup"><span data-stu-id="4bf22-111">The **Remove-WAPackVMRole** cmdlet removes virtual machine role objects.</span></span>

## <span data-ttu-id="4bf22-112">示例</span><span class="sxs-lookup"><span data-stu-id="4bf22-112">EXAMPLES</span></span>

### <span data-ttu-id="4bf22-113">範例1：移除使用 WAP 入口網站建立的虛擬機器角色 () </span><span class="sxs-lookup"><span data-stu-id="4bf22-113">Example 1: Remove a virtual machine role (which was created using the WAP portal)</span></span>
```
PS C:\> $VMRole = Get-WAPackVMRole -Name "ContosoVMRole01"
PS C:\> Remove-WAPackVMRole -VMRole $VMRole
```

<span data-ttu-id="4bf22-114">第一個命令會使用 **WAPackVMRole** Cmdlet 取得名為 ContosoVMRole01 的虛擬機器角色，然後將該物件儲存在 $VMRole 變數中。</span><span class="sxs-lookup"><span data-stu-id="4bf22-114">The first command gets the virtual machine role named ContosoVMRole01 by using the **Get-WAPackVMRole** cmdlet, and then stores that object in the $VMRole variable.</span></span>

<span data-ttu-id="4bf22-115">第二個命令會移除 $VMRole 中儲存的虛擬機器角色。</span><span class="sxs-lookup"><span data-stu-id="4bf22-115">The second command removes the virtual machine role stored in $VMRole.</span></span>
<span data-ttu-id="4bf22-116">命令會提示您進行確認。假設此虛擬機器角色是使用 WAP 入口網站建立的，就不需要指定雲端服務名稱。</span><span class="sxs-lookup"><span data-stu-id="4bf22-116">The command prompts you for confirmation.Assuming this virtual machine role was created using the WAP portal, there's no need to specify the cloud service name.</span></span>

### <span data-ttu-id="4bf22-117">範例2：移除在手動建立雲端服務之後建立的虛擬機器角色</span><span class="sxs-lookup"><span data-stu-id="4bf22-117">Example 2: Remove a virtual machine role which was created after manually creating a cloud service</span></span>
```
PS C:\> $VMRole = Get-WAPackVMRole -Name "ContosoVMRole02"
PS C:\> Remove-WAPackVMRole -VMRole $VMRole -CloudServiceName "ContosoCloudService02"
```

<span data-ttu-id="4bf22-118">第一個命令會使用 **WAPackVMRole** Cmdlet 取得名為 "ContosoVMRole02" 的虛擬機器角色，然後將該物件儲存在 $VMRole 變數中。</span><span class="sxs-lookup"><span data-stu-id="4bf22-118">The first command gets the virtual machine role named "ContosoVMRole02" by using the **Get-WAPackVMRole** cmdlet, and then stores that object in the $VMRole variable.</span></span>

<span data-ttu-id="4bf22-119">第二個命令會移除 $VMRole 中儲存的虛擬機器角色。</span><span class="sxs-lookup"><span data-stu-id="4bf22-119">The second command removes the virtual machine role stored in $VMRole.</span></span>
<span data-ttu-id="4bf22-120">命令會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4bf22-120">The command prompts you for confirmation.</span></span>
<span data-ttu-id="4bf22-121">假設此虛擬機器角色不是使用入口網站建立，則使用者必須指定雲端服務名稱。</span><span class="sxs-lookup"><span data-stu-id="4bf22-121">Assuming this virtual machine role was not created using the portal, the user needs to specify the cloud service name.</span></span>
<span data-ttu-id="4bf22-122">在這種情況下，名為 "ContosoCloudService02"。</span><span class="sxs-lookup"><span data-stu-id="4bf22-122">In this case named "ContosoCloudService02".</span></span>

### <span data-ttu-id="4bf22-123">範例3：移除虛擬機器角色而不進行確認</span><span class="sxs-lookup"><span data-stu-id="4bf22-123">Example 3: Remove a virtual machine role without confirmation</span></span>
```
PS C:\> $VMRole = Get-WAPackVMRole -Name "ContosoVMRole03"
PS C:\> Remove-WAPackVMRole -VMRole $VMRole -Force
```

<span data-ttu-id="4bf22-124">第一個命令會使用 **WAPackVMRole** Cmdlet 取得名為 ContosoVMRole03 的雲端服務，然後將該物件儲存在 $VMRole 變數中。</span><span class="sxs-lookup"><span data-stu-id="4bf22-124">The first command gets the cloud service named ContosoVMRole03 by using the **Get-WAPackVMRole** cmdlet, and then stores that object in the $VMRole variable.</span></span>

<span data-ttu-id="4bf22-125">第二個命令會移除 $VMRole 中儲存的虛擬機器角色。</span><span class="sxs-lookup"><span data-stu-id="4bf22-125">The second command removes the virtual machine role stored in $VMRole.</span></span>
<span data-ttu-id="4bf22-126">這個命令包含 *Force* 參數。</span><span class="sxs-lookup"><span data-stu-id="4bf22-126">This command includes the *Force* parameter.</span></span>
<span data-ttu-id="4bf22-127">該命令不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4bf22-127">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="4bf22-128">參數</span><span class="sxs-lookup"><span data-stu-id="4bf22-128">PARAMETERS</span></span>

### <span data-ttu-id="4bf22-129">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="4bf22-129">-CloudServiceName</span></span>
<span data-ttu-id="4bf22-130">指定虛擬機器角色的雲端服務名稱。</span><span class="sxs-lookup"><span data-stu-id="4bf22-130">Specifies the cloud service name of virtual machine role.</span></span>

```yaml
Type: String
Parameter Sets: FromCloudService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bf22-131">-Force</span><span class="sxs-lookup"><span data-stu-id="4bf22-131">-Force</span></span>
<span data-ttu-id="4bf22-132">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="4bf22-132">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4bf22-133">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4bf22-133">-PassThru</span></span>
<span data-ttu-id="4bf22-134">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="4bf22-134">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="4bf22-135">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="4bf22-135">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="4bf22-136">-設定檔</span><span class="sxs-lookup"><span data-stu-id="4bf22-136">-Profile</span></span>
<span data-ttu-id="4bf22-137">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="4bf22-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4bf22-138">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="4bf22-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4bf22-139">-VMRole</span><span class="sxs-lookup"><span data-stu-id="4bf22-139">-VMRole</span></span>
<span data-ttu-id="4bf22-140">指定虛擬機器角色。</span><span class="sxs-lookup"><span data-stu-id="4bf22-140">Specifies a virtual machine role.</span></span>
<span data-ttu-id="4bf22-141">若要取得虛擬機器角色，請使用 **WAPackVMRole** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4bf22-141">To get a virtual machine role, use the **Get-WAPackVMRole** cmdlet.</span></span>

```yaml
Type: VMRole
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4bf22-142">-確認</span><span class="sxs-lookup"><span data-stu-id="4bf22-142">-Confirm</span></span>
<span data-ttu-id="4bf22-143">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4bf22-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4bf22-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4bf22-144">-WhatIf</span></span>
<span data-ttu-id="4bf22-145">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4bf22-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4bf22-146">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4bf22-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4bf22-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bf22-147">CommonParameters</span></span>
<span data-ttu-id="4bf22-148">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4bf22-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bf22-149">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4bf22-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bf22-150">輸入</span><span class="sxs-lookup"><span data-stu-id="4bf22-150">INPUTS</span></span>

## <span data-ttu-id="4bf22-151">輸出</span><span class="sxs-lookup"><span data-stu-id="4bf22-151">OUTPUTS</span></span>

## <span data-ttu-id="4bf22-152">筆記</span><span class="sxs-lookup"><span data-stu-id="4bf22-152">NOTES</span></span>

## <span data-ttu-id="4bf22-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="4bf22-153">RELATED LINKS</span></span>

[<span data-ttu-id="4bf22-154">WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="4bf22-154">Get-WAPackVMRole</span></span>](./Get-WAPackVMRole.md)

[<span data-ttu-id="4bf22-155">新-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="4bf22-155">New-WAPackVMRole</span></span>](./New-WAPackVMRole.md)

[<span data-ttu-id="4bf22-156">Set-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="4bf22-156">Set-WAPackVMRole</span></span>](./Set-WAPackVMRole.md)


