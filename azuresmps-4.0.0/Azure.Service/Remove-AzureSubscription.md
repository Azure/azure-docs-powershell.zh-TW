---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: ABC303ED-8712-4958-B871-E95357012277
online version: ''
schema: 2.0.0
ms.openlocfilehash: 706c1dee2bc4bb21a8cf116d15bfa3e53daeed99
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967541"
---
# <span data-ttu-id="1e2ac-101">Remove-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="1e2ac-101">Remove-AzureSubscription</span></span>

## <span data-ttu-id="1e2ac-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1e2ac-102">SYNOPSIS</span></span>
<span data-ttu-id="1e2ac-103">從 Windows PowerShell 刪除 Azure 訂閱。</span><span class="sxs-lookup"><span data-stu-id="1e2ac-103">Deletes an Azure subscription from Windows PowerShell.</span></span>

## <span data-ttu-id="1e2ac-104">句法</span><span class="sxs-lookup"><span data-stu-id="1e2ac-104">SYNTAX</span></span>

### <span data-ttu-id="1e2ac-105">預設)  (名稱</span><span class="sxs-lookup"><span data-stu-id="1e2ac-105">Name (Default)</span></span>
```
Remove-AzureSubscription -SubscriptionName <String> [-Force] [-PassThru] [-Profile <AzureSMProfile>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e2ac-106">標識號</span><span class="sxs-lookup"><span data-stu-id="1e2ac-106">Id</span></span>
```
Remove-AzureSubscription -SubscriptionId <String> [-Force] [-PassThru] [-Profile <AzureSMProfile>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e2ac-107">說明</span><span class="sxs-lookup"><span data-stu-id="1e2ac-107">DESCRIPTION</span></span>
<span data-ttu-id="1e2ac-108">**AzureSubscription** Cmdlet 會從您的訂閱資料檔案中刪除 Azure 訂閱，因此 Windows PowerShell 找不到該訂閱。</span><span class="sxs-lookup"><span data-stu-id="1e2ac-108">The **Remove-AzureSubscription** cmdlet deletes an Azure subscription from your subscription data file so Windows PowerShell can't find it.</span></span>
<span data-ttu-id="1e2ac-109">這個 Cmdlet 不會從 Microsoft Azure 刪除訂閱，或以任何方式變更實際的訂閱。</span><span class="sxs-lookup"><span data-stu-id="1e2ac-109">This cmdlet does not delete the subscription from Microsoft Azure, or change the actual subscription in any way.</span></span>

<span data-ttu-id="1e2ac-110">本主題描述 Microsoft Azure PowerShell 模組的0.8.10 版本中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1e2ac-110">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="1e2ac-111">若要取得您正在使用的模組版本，請在 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。</span><span class="sxs-lookup"><span data-stu-id="1e2ac-111">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="1e2ac-112">示例</span><span class="sxs-lookup"><span data-stu-id="1e2ac-112">EXAMPLES</span></span>

### <span data-ttu-id="1e2ac-113">範例1：刪除訂閱</span><span class="sxs-lookup"><span data-stu-id="1e2ac-113">Example 1: Delete a subscription</span></span>
```
C:\PS> Remove-AzureSubscription -SubscriptionName Test

Confirm
Are you sure you want to perform this action?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"):
```

<span data-ttu-id="1e2ac-114">這個命令會從預設的訂閱資料檔案刪除「測試」訂閱。</span><span class="sxs-lookup"><span data-stu-id="1e2ac-114">This command deletes the "Test" subscription from the default subscription data file.</span></span>

### <span data-ttu-id="1e2ac-115">範例2：從替代訂閱資料檔案中刪除</span><span class="sxs-lookup"><span data-stu-id="1e2ac-115">Example 2: Delete from an alternate subscription data file</span></span>
```
C:\PS> Remove-AzureSubscription -SubscriptionName Test -SubscriptionDataFile C:\Subs\MySubscriptions.xml -Force
```

<span data-ttu-id="1e2ac-116">這個命令會從 MySubscriptions.xml 訂閱資料檔案刪除測試訂閱。</span><span class="sxs-lookup"><span data-stu-id="1e2ac-116">This command deletes the Test subscription from the MySubscriptions.xml subscription data file.</span></span>
<span data-ttu-id="1e2ac-117">命令會使用 *Force* 參數來取消確認提示。</span><span class="sxs-lookup"><span data-stu-id="1e2ac-117">The command uses the *Force* parameter to suppress the confirmation prompt.</span></span>

### <span data-ttu-id="1e2ac-118">範例3：在腳本中刪除訂閱</span><span class="sxs-lookup"><span data-stu-id="1e2ac-118">Example 3: Delete a subscription in a script</span></span>
```
C:\PS> ...if (Remove-AzureSubscription -SubscriptionName Test -PassThru) {...}
```

<span data-ttu-id="1e2ac-119">這個命令在 **If** 語句中使用 [ **移除-AzureSubscription** ] 命令。</span><span class="sxs-lookup"><span data-stu-id="1e2ac-119">This command uses the **Remove-AzureSubscription** command in an **If** statement.</span></span>
<span data-ttu-id="1e2ac-120">它會使用 *PassThru* 參數（傳回布林值）來判斷 **If** 語句中的腳本區塊是否已執行。</span><span class="sxs-lookup"><span data-stu-id="1e2ac-120">It uses the *PassThru* parameter, which returns a Boolean value, to determine whether the script block in the **If** statement is executed.</span></span>

## <span data-ttu-id="1e2ac-121">參數</span><span class="sxs-lookup"><span data-stu-id="1e2ac-121">PARAMETERS</span></span>

### <span data-ttu-id="1e2ac-122">-Force</span><span class="sxs-lookup"><span data-stu-id="1e2ac-122">-Force</span></span>
<span data-ttu-id="1e2ac-123">取消確認提示。</span><span class="sxs-lookup"><span data-stu-id="1e2ac-123">Suppresses the confirmation prompt.</span></span>

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

### <span data-ttu-id="1e2ac-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1e2ac-124">-PassThru</span></span>
<span data-ttu-id="1e2ac-125">如果命令成功，則傳回 $True，且 $False 失敗。</span><span class="sxs-lookup"><span data-stu-id="1e2ac-125">Returns $True if the command succeeds and $False if it fails.</span></span>
<span data-ttu-id="1e2ac-126">根據預設，這個 Cmdlet 不會傳回任何輸出。</span><span class="sxs-lookup"><span data-stu-id="1e2ac-126">By default, this cmdlet does not return any output.</span></span>

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

### <span data-ttu-id="1e2ac-127">-設定檔</span><span class="sxs-lookup"><span data-stu-id="1e2ac-127">-Profile</span></span>
<span data-ttu-id="1e2ac-128">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="1e2ac-128">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="1e2ac-129">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="1e2ac-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1e2ac-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1e2ac-130">-SubscriptionId</span></span>
```yaml
Type: String
Parameter Sets: Id
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e2ac-131">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="1e2ac-131">-SubscriptionName</span></span>
```yaml
Type: String
Parameter Sets: Name
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e2ac-132">-確認</span><span class="sxs-lookup"><span data-stu-id="1e2ac-132">-Confirm</span></span>
<span data-ttu-id="1e2ac-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1e2ac-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e2ac-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e2ac-134">-WhatIf</span></span>
<span data-ttu-id="1e2ac-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1e2ac-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e2ac-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1e2ac-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e2ac-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e2ac-137">CommonParameters</span></span>
<span data-ttu-id="1e2ac-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1e2ac-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e2ac-139">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1e2ac-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e2ac-140">輸入</span><span class="sxs-lookup"><span data-stu-id="1e2ac-140">INPUTS</span></span>

### <span data-ttu-id="1e2ac-141">所有</span><span class="sxs-lookup"><span data-stu-id="1e2ac-141">None</span></span>
<span data-ttu-id="1e2ac-142">您可以透過屬性名稱（而不是依值），將輸入管到這個 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1e2ac-142">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="1e2ac-143">輸出</span><span class="sxs-lookup"><span data-stu-id="1e2ac-143">OUTPUTS</span></span>

### <span data-ttu-id="1e2ac-144">None 或 System.object</span><span class="sxs-lookup"><span data-stu-id="1e2ac-144">None or System.Boolean</span></span>
<span data-ttu-id="1e2ac-145">如果您使用 *PassThru* 參數，這個 Cmdlet 會傳回布林值。</span><span class="sxs-lookup"><span data-stu-id="1e2ac-145">If you use the *PassThru* parameter, this cmdlet returns a Boolean value.</span></span>
<span data-ttu-id="1e2ac-146">否則，它不會傳回任何輸出。</span><span class="sxs-lookup"><span data-stu-id="1e2ac-146">Otherwise, it does not return any output.</span></span>

## <span data-ttu-id="1e2ac-147">筆記</span><span class="sxs-lookup"><span data-stu-id="1e2ac-147">NOTES</span></span>

## <span data-ttu-id="1e2ac-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="1e2ac-148">RELATED LINKS</span></span>

[<span data-ttu-id="1e2ac-149">AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="1e2ac-149">Get-AzureSubscription</span></span>](./Get-AzureSubscription.md)

[<span data-ttu-id="1e2ac-150">選取-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="1e2ac-150">Select-AzureSubscription</span></span>](./Select-AzureSubscription.md)

[<span data-ttu-id="1e2ac-151">Set-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="1e2ac-151">Set-AzureSubscription</span></span>](./Set-AzureSubscription.md)


