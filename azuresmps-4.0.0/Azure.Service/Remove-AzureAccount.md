---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 3CD1A989-902C-48B3-81E9-7B78EDA5F880
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7003abf263fd4c669956f65c990246295cf7158d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967316"
---
# <span data-ttu-id="e94f1-101">Remove-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="e94f1-101">Remove-AzureAccount</span></span>

## <span data-ttu-id="e94f1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e94f1-102">SYNOPSIS</span></span>
<span data-ttu-id="e94f1-103">從 Windows PowerShell 刪除 Azure 帳戶。</span><span class="sxs-lookup"><span data-stu-id="e94f1-103">Deletes an Azure account from Windows PowerShell.</span></span>

## <span data-ttu-id="e94f1-104">句法</span><span class="sxs-lookup"><span data-stu-id="e94f1-104">SYNTAX</span></span>

```
Remove-AzureAccount -Name <String> [-Force] [-PassThru] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e94f1-105">說明</span><span class="sxs-lookup"><span data-stu-id="e94f1-105">DESCRIPTION</span></span>
<span data-ttu-id="e94f1-106">**AzureAccount** Cmdlet 會從您漫遊使用者設定檔中的訂閱資料檔刪除 Azure 帳戶及其訂閱。</span><span class="sxs-lookup"><span data-stu-id="e94f1-106">The **Remove-AzureAccount** cmdlet deletes an Azure account and its subscriptions from the subscription data file in your roaming user profile.</span></span>
<span data-ttu-id="e94f1-107">它不會從 Microsoft Azure 刪除帳戶，或以任何方式變更實際的帳戶。</span><span class="sxs-lookup"><span data-stu-id="e94f1-107">It does not delete the account from Microsoft Azure, or change the actual account in any way.</span></span>

<span data-ttu-id="e94f1-108">使用這個 Cmdlet 很像是從您的 Azure 帳戶登入。</span><span class="sxs-lookup"><span data-stu-id="e94f1-108">Using this cmdlet is a lot like logging out of your Azure account.</span></span>
<span data-ttu-id="e94f1-109">而且，如果您想要再次登入帳戶，請使用 [ **載入 AzureAccount** ] 或 [匯 **入-AzurePublishSettingsFile** ]，將該帳戶再次新增至 Windows PowerShell。</span><span class="sxs-lookup"><span data-stu-id="e94f1-109">And, if you want to log into the account again, use the **Add-AzureAccount** or **Import-AzurePublishSettingsFile** to add the account to Windows PowerShell again.</span></span>

<span data-ttu-id="e94f1-110">您也可以使用 **AzureAccount** Cmdlet 來變更 azure PowerShell Cmdlet 登入 azure 帳戶的方式。</span><span class="sxs-lookup"><span data-stu-id="e94f1-110">You can also use **Remove-AzureAccount** cmdlet to change the way the Azure PowerShell cmdlets sign into your Azure account.</span></span>
<span data-ttu-id="e94f1-111">如果您的帳戶同時有來自 **Import AzurePublishSettingsFile** 的管理憑證和來自 **Add AzureAccount** 的存取權杖，則 Azure PowerShell Cmdlet 只會使用存取權杖;它們會忽略管理憑證。</span><span class="sxs-lookup"><span data-stu-id="e94f1-111">If your account has both a management certificate from **Import-AzurePublishSettingsFile** and an access token from **Add-AzureAccount** , the Azure PowerShell cmdlets use only the access token; they ignore the management certificate.</span></span>
<span data-ttu-id="e94f1-112">若要使用管理憑證，請執行 **移除-AzureAccount** 。</span><span class="sxs-lookup"><span data-stu-id="e94f1-112">To use the management certificate, run **Remove-AzureAccount**.</span></span>
<span data-ttu-id="e94f1-113">當 **AzureAccount** 發現管理憑證和存取權杖時，只會刪除存取權杖，而不會刪除帳戶。</span><span class="sxs-lookup"><span data-stu-id="e94f1-113">When **Remove-AzureAccount** finds both a management certificate and an access token, it deletes only the access token, instead of deleting the account.</span></span>
<span data-ttu-id="e94f1-114">管理憑證仍然存在，因此 Windows PowerShell 仍可使用帳戶。</span><span class="sxs-lookup"><span data-stu-id="e94f1-114">The management certificate is still there, so account is still available to Windows PowerShell.</span></span>

<span data-ttu-id="e94f1-115">本主題描述 Microsoft Azure PowerShell 模組的0.8.10 版本中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e94f1-115">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="e94f1-116">若要取得您正在使用的模組版本，請在 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。</span><span class="sxs-lookup"><span data-stu-id="e94f1-116">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="e94f1-117">示例</span><span class="sxs-lookup"><span data-stu-id="e94f1-117">EXAMPLES</span></span>

### <span data-ttu-id="e94f1-118">範例1：移除帳戶</span><span class="sxs-lookup"><span data-stu-id="e94f1-118">Example 1: Remove an account</span></span>
```
PS C:\> Remove-AzureAccount -Name admin@contoso.com
```

<span data-ttu-id="e94f1-119">這個命令會 admin@contoso.com 從您的訂閱資料檔案中移除。</span><span class="sxs-lookup"><span data-stu-id="e94f1-119">This command removes the admin@contoso.com from your subscription data file.</span></span>
<span data-ttu-id="e94f1-120">命令完成後，Windows PowerShell 將無法再使用該帳戶。</span><span class="sxs-lookup"><span data-stu-id="e94f1-120">When the command completes, the account is no longer available to Windows PowerShell.</span></span>

## <span data-ttu-id="e94f1-121">參數</span><span class="sxs-lookup"><span data-stu-id="e94f1-121">PARAMETERS</span></span>

### <span data-ttu-id="e94f1-122">-Force</span><span class="sxs-lookup"><span data-stu-id="e94f1-122">-Force</span></span>
<span data-ttu-id="e94f1-123">取消確認提示。</span><span class="sxs-lookup"><span data-stu-id="e94f1-123">Suppresses the confirmation prompt.</span></span>
<span data-ttu-id="e94f1-124">根據預設， **AzureAccount** 會在您從 Windows PowerShell 移除帳戶之前提示您。</span><span class="sxs-lookup"><span data-stu-id="e94f1-124">By default, **Remove-AzureAccount** prompts you before removing the account from Windows PowerShell.</span></span>

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

### <span data-ttu-id="e94f1-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="e94f1-125">-Name</span></span>
<span data-ttu-id="e94f1-126">指定要移除的帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="e94f1-126">Specifies the name of the account to remove.</span></span>
<span data-ttu-id="e94f1-127">參數值區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="e94f1-127">The parameter value is case-sensitive.</span></span>
<span data-ttu-id="e94f1-128">不支援萬用字元。</span><span class="sxs-lookup"><span data-stu-id="e94f1-128">Wildcard characters are not supported.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e94f1-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e94f1-129">-PassThru</span></span>
<span data-ttu-id="e94f1-130">如果命令成功，則傳回 $True，且 $False 失敗。</span><span class="sxs-lookup"><span data-stu-id="e94f1-130">Returns $True if the command succeeds and $False if it fails.</span></span>
<span data-ttu-id="e94f1-131">根據預設，這個 Cmdlet 不會傳回任何輸出。</span><span class="sxs-lookup"><span data-stu-id="e94f1-131">By default, this cmdlet does not return any output.</span></span>

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

### <span data-ttu-id="e94f1-132">-設定檔</span><span class="sxs-lookup"><span data-stu-id="e94f1-132">-Profile</span></span>
<span data-ttu-id="e94f1-133">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="e94f1-133">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="e94f1-134">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="e94f1-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e94f1-135">-確認</span><span class="sxs-lookup"><span data-stu-id="e94f1-135">-Confirm</span></span>
<span data-ttu-id="e94f1-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e94f1-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e94f1-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e94f1-137">-WhatIf</span></span>
<span data-ttu-id="e94f1-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e94f1-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e94f1-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e94f1-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e94f1-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e94f1-140">CommonParameters</span></span>
<span data-ttu-id="e94f1-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e94f1-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e94f1-142">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e94f1-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e94f1-143">輸入</span><span class="sxs-lookup"><span data-stu-id="e94f1-143">INPUTS</span></span>

### <span data-ttu-id="e94f1-144">所有</span><span class="sxs-lookup"><span data-stu-id="e94f1-144">None</span></span>
<span data-ttu-id="e94f1-145">您可以透過屬性名稱（而不是依值），將輸入管到這個 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e94f1-145">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="e94f1-146">輸出</span><span class="sxs-lookup"><span data-stu-id="e94f1-146">OUTPUTS</span></span>

### <span data-ttu-id="e94f1-147">None 或 System.object</span><span class="sxs-lookup"><span data-stu-id="e94f1-147">None or System.Boolean</span></span>
<span data-ttu-id="e94f1-148">如果您使用 *PassThru* 參數，這個 Cmdlet 會傳回布林值。</span><span class="sxs-lookup"><span data-stu-id="e94f1-148">If you use the *PassThru* parameter, this cmdlet returns a Boolean value.</span></span>
<span data-ttu-id="e94f1-149">否則，它不會傳回任何輸出。</span><span class="sxs-lookup"><span data-stu-id="e94f1-149">Otherwise, it does not return any output.</span></span>

## <span data-ttu-id="e94f1-150">筆記</span><span class="sxs-lookup"><span data-stu-id="e94f1-150">NOTES</span></span>

## <span data-ttu-id="e94f1-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="e94f1-151">RELATED LINKS</span></span>

[<span data-ttu-id="e94f1-152">附加 AzureAccount</span><span class="sxs-lookup"><span data-stu-id="e94f1-152">Add-AzureAccount</span></span>](./Add-AzureAccount.md)

[<span data-ttu-id="e94f1-153">AzureAccount</span><span class="sxs-lookup"><span data-stu-id="e94f1-153">Get-AzureAccount</span></span>](./Get-AzureAccount.md)


