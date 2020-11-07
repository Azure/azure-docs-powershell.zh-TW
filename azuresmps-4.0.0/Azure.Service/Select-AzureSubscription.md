---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 7A45DCAD-88DC-40F0-BBF7-0F531A571CA6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 48b941691366c3af821e3a4cdaa7b07c5e958e16
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93966891"
---
# <span data-ttu-id="9c9a4-101">Select-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="9c9a4-101">Select-AzureSubscription</span></span>

## <span data-ttu-id="9c9a4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9c9a4-102">SYNOPSIS</span></span>
<span data-ttu-id="9c9a4-103">變更目前和預設的 Azure 訂閱。</span><span class="sxs-lookup"><span data-stu-id="9c9a4-103">Changes the current and default Azure subscriptions.</span></span>

## <span data-ttu-id="9c9a4-104">句法</span><span class="sxs-lookup"><span data-stu-id="9c9a4-104">SYNTAX</span></span>

### <span data-ttu-id="9c9a4-105">SelectSubscriptionByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="9c9a4-105">SelectSubscriptionByNameParameterSet (Default)</span></span>
```
Select-AzureSubscription -SubscriptionName <String> [-Account <String>] [-Current] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="9c9a4-106">SelectDefaultSubscriptionByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9c9a4-106">SelectDefaultSubscriptionByNameParameterSet</span></span>
```
Select-AzureSubscription -SubscriptionName <String> [-Account <String>] [-Default] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="9c9a4-107">SelectSubscriptionByIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9c9a4-107">SelectSubscriptionByIdParameterSet</span></span>
```
Select-AzureSubscription -SubscriptionId <String> [-Account <String>] [-Current] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="9c9a4-108">SelectDefaultSubscriptionByIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9c9a4-108">SelectDefaultSubscriptionByIdParameterSet</span></span>
```
Select-AzureSubscription -SubscriptionId <String> [-Account <String>] [-Default] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="9c9a4-109">NoCurrentSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="9c9a4-109">NoCurrentSubscriptionParameterSet</span></span>
```
Select-AzureSubscription [-Account <String>] [-NoCurrent] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="9c9a4-110">NoDefaultSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="9c9a4-110">NoDefaultSubscriptionParameterSet</span></span>
```
Select-AzureSubscription [-Account <String>] [-NoDefault] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="9c9a4-111">說明</span><span class="sxs-lookup"><span data-stu-id="9c9a4-111">DESCRIPTION</span></span>
<span data-ttu-id="9c9a4-112">**AzureSubscription** Cmdlet 會設定並清除目前和預設的 Azure 訂閱。</span><span class="sxs-lookup"><span data-stu-id="9c9a4-112">The **Select-AzureSubscription** cmdlet sets and clears the current and default Azure subscriptions.</span></span>

<span data-ttu-id="9c9a4-113">[目前訂閱] 是目前 Windows PowerShell 會話中預設使用的訂閱。</span><span class="sxs-lookup"><span data-stu-id="9c9a4-113">The "current subscription" is the subscription that is used by default in the current Windows PowerShell session.</span></span>
<span data-ttu-id="9c9a4-114">[預設訂閱] 預設會在所有 Windows PowerShell 會話中使用。</span><span class="sxs-lookup"><span data-stu-id="9c9a4-114">The "default subscription" is used by default in all Windows PowerShell sessions.</span></span>
<span data-ttu-id="9c9a4-115">[目前的訂閱] 標籤可讓您指定不同的訂閱供預設用於目前會話，而不會變更所有其他會話的「預設訂閱」。</span><span class="sxs-lookup"><span data-stu-id="9c9a4-115">The "current subscription" label lets you specify a different subscription to be used by default for the current session without changing the "default subscription" for all other sessions.</span></span>

<span data-ttu-id="9c9a4-116">"預設" 訂閱指定會儲存在您的訂閱資料檔案中。</span><span class="sxs-lookup"><span data-stu-id="9c9a4-116">The "default" subscription designation is saved in your subscription data file.</span></span>
<span data-ttu-id="9c9a4-117">不會儲存會話特定的「目前」指派。</span><span class="sxs-lookup"><span data-stu-id="9c9a4-117">The session-specific "current" designation is not saved.</span></span>

<span data-ttu-id="9c9a4-118">本主題描述 Microsoft Azure PowerShell 模組的0.8.10 版本中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9c9a4-118">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="9c9a4-119">若要取得您正在使用的模組版本，請在 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。</span><span class="sxs-lookup"><span data-stu-id="9c9a4-119">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="9c9a4-120">示例</span><span class="sxs-lookup"><span data-stu-id="9c9a4-120">EXAMPLES</span></span>

### <span data-ttu-id="9c9a4-121">範例1：設定目前的訂閱</span><span class="sxs-lookup"><span data-stu-id="9c9a4-121">Example 1: Set the current subscription</span></span>
```
C:\PS> Select-AzureSubscription -Current -SubscriptionName ContosoEngineering
```

<span data-ttu-id="9c9a4-122">這個命令會將「ContosoEngineering」做為目前的訂閱。</span><span class="sxs-lookup"><span data-stu-id="9c9a4-122">This command makes "ContosoEngineering" the current subscription.</span></span>

### <span data-ttu-id="9c9a4-123">範例2：設定預設訂閱</span><span class="sxs-lookup"><span data-stu-id="9c9a4-123">Example 2: Set the default subscription</span></span>
```
C:\PS> Select-AzureSubscription -Default -SubscriptionName ContosoFinance -SubscriptionDataFile "C:\subs\MySubscriptions.xml"
```

<span data-ttu-id="9c9a4-124">這個命令會將預設訂閱變更為「ContosoFinance」。</span><span class="sxs-lookup"><span data-stu-id="9c9a4-124">This command changes the default subscription to "ContosoFinance."</span></span> <span data-ttu-id="9c9a4-125">它會將設定儲存在 Subscriptions.xml 訂閱資料檔中，而不是預設的訂閱資料檔案。</span><span class="sxs-lookup"><span data-stu-id="9c9a4-125">It saves the setting in the Subscriptions.xml subscription data file, instead of the default subscription data file.</span></span>

## <span data-ttu-id="9c9a4-126">參數</span><span class="sxs-lookup"><span data-stu-id="9c9a4-126">PARAMETERS</span></span>

### <span data-ttu-id="9c9a4-127">-帳戶</span><span class="sxs-lookup"><span data-stu-id="9c9a4-127">-Account</span></span>
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

### <span data-ttu-id="9c9a4-128">-目前</span><span class="sxs-lookup"><span data-stu-id="9c9a4-128">-Current</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: SelectSubscriptionByNameParameterSet, SelectSubscriptionByIdParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c9a4-129">-預設值</span><span class="sxs-lookup"><span data-stu-id="9c9a4-129">-Default</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: SelectDefaultSubscriptionByNameParameterSet, SelectDefaultSubscriptionByIdParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c9a4-130">-NoCurrent</span><span class="sxs-lookup"><span data-stu-id="9c9a4-130">-NoCurrent</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: NoCurrentSubscriptionParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c9a4-131">-NoDefault</span><span class="sxs-lookup"><span data-stu-id="9c9a4-131">-NoDefault</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: NoDefaultSubscriptionParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c9a4-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9c9a4-132">-PassThru</span></span>
<span data-ttu-id="9c9a4-133">如果命令成功，則傳回 $True，且 $False 失敗。</span><span class="sxs-lookup"><span data-stu-id="9c9a4-133">Returns $True if the command succeeds and $False if it fails.</span></span>
<span data-ttu-id="9c9a4-134">根據預設，這個 Cmdlet 不會傳回任何輸出。</span><span class="sxs-lookup"><span data-stu-id="9c9a4-134">By default, this cmdlet does not return any output.</span></span>

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

### <span data-ttu-id="9c9a4-135">-設定檔</span><span class="sxs-lookup"><span data-stu-id="9c9a4-135">-Profile</span></span>
<span data-ttu-id="9c9a4-136">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="9c9a4-136">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="9c9a4-137">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="9c9a4-137">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9c9a4-138">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9c9a4-138">-SubscriptionId</span></span>
```yaml
Type: String
Parameter Sets: SelectSubscriptionByIdParameterSet, SelectDefaultSubscriptionByIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c9a4-139">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="9c9a4-139">-SubscriptionName</span></span>
```yaml
Type: String
Parameter Sets: SelectSubscriptionByNameParameterSet, SelectDefaultSubscriptionByNameParameterSet
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c9a4-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c9a4-140">CommonParameters</span></span>
<span data-ttu-id="9c9a4-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9c9a4-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c9a4-142">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9c9a4-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c9a4-143">輸入</span><span class="sxs-lookup"><span data-stu-id="9c9a4-143">INPUTS</span></span>

### <span data-ttu-id="9c9a4-144">所有</span><span class="sxs-lookup"><span data-stu-id="9c9a4-144">None</span></span>
<span data-ttu-id="9c9a4-145">您可以透過屬性名稱（而不是依值），將輸入管到這個 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9c9a4-145">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="9c9a4-146">輸出</span><span class="sxs-lookup"><span data-stu-id="9c9a4-146">OUTPUTS</span></span>

### <span data-ttu-id="9c9a4-147">None 或 System.object</span><span class="sxs-lookup"><span data-stu-id="9c9a4-147">None or System.Boolean</span></span>
<span data-ttu-id="9c9a4-148">如果您使用 *PassThru* 參數，這個 Cmdlet 會傳回布林值。</span><span class="sxs-lookup"><span data-stu-id="9c9a4-148">If you use the *PassThru* parameter, this cmdlet returns a Boolean value.</span></span>
<span data-ttu-id="9c9a4-149">根據預設，它不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="9c9a4-149">By default, it does not generate any output.</span></span>

## <span data-ttu-id="9c9a4-150">筆記</span><span class="sxs-lookup"><span data-stu-id="9c9a4-150">NOTES</span></span>

## <span data-ttu-id="9c9a4-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="9c9a4-151">RELATED LINKS</span></span>

[<span data-ttu-id="9c9a4-152">AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="9c9a4-152">Get-AzureSubscription</span></span>](./Get-AzureSubscription.md)

[<span data-ttu-id="9c9a4-153">移除-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="9c9a4-153">Remove-AzureSubscription</span></span>](./Remove-AzureSubscription.md)

[<span data-ttu-id="9c9a4-154">Set-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="9c9a4-154">Set-AzureSubscription</span></span>](./Set-AzureSubscription.md)


