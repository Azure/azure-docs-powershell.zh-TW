---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 32BC6CE6-60EF-4A46-912B-8FE4FCCDF7CC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2b91906a25d2f2d7c40f96ed07a4fd7463722023
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93966983"
---
# <span data-ttu-id="1b72e-101">Get-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="1b72e-101">Get-AzureSubscription</span></span>

## <span data-ttu-id="1b72e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1b72e-102">SYNOPSIS</span></span>
<span data-ttu-id="1b72e-103">取得 Azure 帳戶中的 Azure 訂閱。</span><span class="sxs-lookup"><span data-stu-id="1b72e-103">Gets  Azure subscriptions in Azure account.</span></span>

## <span data-ttu-id="1b72e-104">句法</span><span class="sxs-lookup"><span data-stu-id="1b72e-104">SYNTAX</span></span>

### <span data-ttu-id="1b72e-105">ByName (預設) </span><span class="sxs-lookup"><span data-stu-id="1b72e-105">ByName (Default)</span></span>
```
Get-AzureSubscription [-SubscriptionName <String>] [-ExtendedDetails] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="1b72e-106">ById</span><span class="sxs-lookup"><span data-stu-id="1b72e-106">ById</span></span>
```
Get-AzureSubscription [-SubscriptionId <String>] [-ExtendedDetails] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="1b72e-107">設置</span><span class="sxs-lookup"><span data-stu-id="1b72e-107">Default</span></span>
```
Get-AzureSubscription [-Default] [-ExtendedDetails] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="1b72e-108">當前</span><span class="sxs-lookup"><span data-stu-id="1b72e-108">Current</span></span>
```
Get-AzureSubscription [-Current] [-ExtendedDetails] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="1b72e-109">說明</span><span class="sxs-lookup"><span data-stu-id="1b72e-109">DESCRIPTION</span></span>
<span data-ttu-id="1b72e-110">**AzureSubscription** Cmdlet 會在您的 Azure 帳戶中取得訂閱。</span><span class="sxs-lookup"><span data-stu-id="1b72e-110">The **Get-AzureSubscription** cmdlet gets the subscriptions in your Azure account.</span></span>
<span data-ttu-id="1b72e-111">您可以使用這個 Cmdlet 來取得訂閱的相關資訊，以及將訂閱傳送給其他 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1b72e-111">You can use this cmdlet to get information about the subscription and to pipe the subscription to other cmdlets.</span></span>

<span data-ttu-id="1b72e-112">**AzureSubscription** 需要存取您的 Azure 帳戶。</span><span class="sxs-lookup"><span data-stu-id="1b72e-112">**Get-AzureSubscription** requires access to your Azure accounts.</span></span>
<span data-ttu-id="1b72e-113">在執行 **AzureSubscription** 之前，您必須執行 **AzureAccount** Cmdlet 或下載並安裝發佈設定檔案的 Cmdlet， ( **AzurePublishSettingsFile** 、 **Import-AzurePublishSettingsFile** 。</span><span class="sxs-lookup"><span data-stu-id="1b72e-113">Before you run **Get-AzureSubscription** , you must run the **Add-AzureAccount** cmdlet or the cmdlets that download and install a publish settings file ( **Get-AzurePublishSettingsFile** , **Import-AzurePublishSettingsFile**.</span></span>

<span data-ttu-id="1b72e-114">本主題描述 Microsoft Azure PowerShell 模組的0.8.10 版本中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1b72e-114">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="1b72e-115">若要取得您正在使用的模組版本，請在 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。</span><span class="sxs-lookup"><span data-stu-id="1b72e-115">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="1b72e-116">示例</span><span class="sxs-lookup"><span data-stu-id="1b72e-116">EXAMPLES</span></span>

### <span data-ttu-id="1b72e-117">範例1：取得所有訂閱</span><span class="sxs-lookup"><span data-stu-id="1b72e-117">Example 1: Get all subscriptions</span></span>
```
C:\PS>Get-AzureSubscription
```

<span data-ttu-id="1b72e-118">這個命令會取得帳戶中的所有訂閱。</span><span class="sxs-lookup"><span data-stu-id="1b72e-118">This command gets all subscriptions in the account.</span></span>

### <span data-ttu-id="1b72e-119">範例2：依名稱取得訂閱</span><span class="sxs-lookup"><span data-stu-id="1b72e-119">Example 2: Get a subscription by name</span></span>
```
C:\PS>Get-AzureSubscription -SubscriptionName "MyProdSubscription"
```

<span data-ttu-id="1b72e-120">這個命令只會取得「MyProdSubsciption」訂閱。</span><span class="sxs-lookup"><span data-stu-id="1b72e-120">This command gets only the "MyProdSubsciption" subscription.</span></span>

### <span data-ttu-id="1b72e-121">範例3：取得預設訂閱</span><span class="sxs-lookup"><span data-stu-id="1b72e-121">Example 3: Get the default subscription</span></span>
```
C:\PS>(Get-AzureSubscription -Default).SubscriptionName
```

<span data-ttu-id="1b72e-122">這個命令只會取得預設訂閱的名稱。</span><span class="sxs-lookup"><span data-stu-id="1b72e-122">This command gets only the name of the default subscription.</span></span>
<span data-ttu-id="1b72e-123">命令會先取得訂閱，然後使用 dot 方法取得訂閱的 **SubscriptionName** 屬性。</span><span class="sxs-lookup"><span data-stu-id="1b72e-123">The command first gets the subscription and then uses the dot method to get the **SubscriptionName** property of the subscription.</span></span>

### <span data-ttu-id="1b72e-124">範例4：取得選取的訂閱屬性</span><span class="sxs-lookup"><span data-stu-id="1b72e-124">Example 4: Get selected subscription properties</span></span>
```
C:\PS>Get-AzureSubscription -Current | Format-List -Property SubscriptionName, Certificate
```

<span data-ttu-id="1b72e-125">這個命令會傳回含有目前訂閱之名稱和憑證的清單。</span><span class="sxs-lookup"><span data-stu-id="1b72e-125">This command returns a list with the name and certificate of the current subscription.</span></span>
<span data-ttu-id="1b72e-126">它使用 **AzureSubscription** 命令來取得目前的訂閱。</span><span class="sxs-lookup"><span data-stu-id="1b72e-126">It uses a **Get-AzureSubscription** command to get the current subscription.</span></span>
<span data-ttu-id="1b72e-127">接著，它會將訂閱的 [ **格式化清單** ] 命令，以顯示清單中選取的屬性。</span><span class="sxs-lookup"><span data-stu-id="1b72e-127">Then it pipes the subscription to a **Format-List** command that displays the selected properties in a list.</span></span>

### <span data-ttu-id="1b72e-128">範例5：使用替代訂閱資料檔案</span><span class="sxs-lookup"><span data-stu-id="1b72e-128">Example 5: Use an alternate subscription data file</span></span>
```
C:\PS>Get-AzureSubscription -SubscriptionDataFile "C:\Temp\MySubscriptions.xml"
```

<span data-ttu-id="1b72e-129">這個命令會從 C:\Temp\MySubscriptions.xml 訂閱資料檔案中取得訂閱。</span><span class="sxs-lookup"><span data-stu-id="1b72e-129">This command gets subscriptions from  the C:\Temp\MySubscriptions.xml subscription data file.</span></span>
<span data-ttu-id="1b72e-130">如果您在執行 [ **載入 AzureAccount** ] 或 [匯 **入 PublishSettingsFile** ] Cmdlet 時指定了備用訂閱資料檔案，請使用 **SubscriptionDataFile** 參數。</span><span class="sxs-lookup"><span data-stu-id="1b72e-130">Use the **SubscriptionDataFile** parameter if you specified an alternate subscription data file when you ran the **Add-AzureAccount** or **Import-PublishSettingsFile** cmdlets.</span></span>

## <span data-ttu-id="1b72e-131">參數</span><span class="sxs-lookup"><span data-stu-id="1b72e-131">PARAMETERS</span></span>

### <span data-ttu-id="1b72e-132">-目前</span><span class="sxs-lookup"><span data-stu-id="1b72e-132">-Current</span></span>
<span data-ttu-id="1b72e-133">只取得目前的訂閱，也就是指派為「目前」的訂閱。</span><span class="sxs-lookup"><span data-stu-id="1b72e-133">Gets only the current subscription, that is, the subscription designated as "current."</span></span> <span data-ttu-id="1b72e-134">根據預設， **AzureSubscription** 會在您的 Azure 帳戶中取得所有訂閱。</span><span class="sxs-lookup"><span data-stu-id="1b72e-134">By default, **Get-AzureSubscription** gets all subscriptions in your Azure accounts.</span></span>
<span data-ttu-id="1b72e-135">若要將訂閱指定為「目前」，請使用 **AzureSubscription** Cmdlet 的 **目前** 參數。</span><span class="sxs-lookup"><span data-stu-id="1b72e-135">To designate a subscription as "current," use the **Current** parameter of the **Select-AzureSubscription** cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Current
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b72e-136">-預設值</span><span class="sxs-lookup"><span data-stu-id="1b72e-136">-Default</span></span>
<span data-ttu-id="1b72e-137">只取得預設訂閱，也就是指派為「預設」的訂閱。</span><span class="sxs-lookup"><span data-stu-id="1b72e-137">Gets only the default subscription, that is, the subscription designated as "default."</span></span> <span data-ttu-id="1b72e-138">根據預設， **AzureSubscription** 會在您的 Azure 帳戶中取得所有訂閱。</span><span class="sxs-lookup"><span data-stu-id="1b72e-138">By default, **Get-AzureSubscription** gets all subscriptions in your Azure accounts.</span></span>
<span data-ttu-id="1b72e-139">若要將訂閱指定為「預設」，請使用 **AzureSubscription** Cmdlet 的 **預設** 參數。</span><span class="sxs-lookup"><span data-stu-id="1b72e-139">To designate a subscription as "default," use the **Default** parameter of the **Select-AzureSubscription** cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Default
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b72e-140">-ExtendedDetails</span><span class="sxs-lookup"><span data-stu-id="1b72e-140">-ExtendedDetails</span></span>
<span data-ttu-id="1b72e-141">除了標準設定之外，還會傳回訂閱的配額資訊。</span><span class="sxs-lookup"><span data-stu-id="1b72e-141">Returns quota information for the subscription, in addition to the standard settings.</span></span>

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

### <span data-ttu-id="1b72e-142">-設定檔</span><span class="sxs-lookup"><span data-stu-id="1b72e-142">-Profile</span></span>
<span data-ttu-id="1b72e-143">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="1b72e-143">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="1b72e-144">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="1b72e-144">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1b72e-145">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1b72e-145">-SubscriptionId</span></span>
```yaml
Type: String
Parameter Sets: ById
Aliases: Id

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b72e-146">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="1b72e-146">-SubscriptionName</span></span>
<span data-ttu-id="1b72e-147">只取得指定的訂閱。</span><span class="sxs-lookup"><span data-stu-id="1b72e-147">Gets only the specified subscription.</span></span>
<span data-ttu-id="1b72e-148">輸入訂閱名稱。</span><span class="sxs-lookup"><span data-stu-id="1b72e-148">Enter the subscription name.</span></span>
<span data-ttu-id="1b72e-149">此值區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="1b72e-149">The value is case-sensitive.</span></span>
<span data-ttu-id="1b72e-150">不支援萬用字元。</span><span class="sxs-lookup"><span data-stu-id="1b72e-150">Wildcard characters are not supported.</span></span>
<span data-ttu-id="1b72e-151">根據預設， **AzureSubscription** 會在您的 Azure 帳戶中取得所有訂閱。</span><span class="sxs-lookup"><span data-stu-id="1b72e-151">By default, **Get-AzureSubscription** gets all subscriptions in your Azure accounts.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b72e-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b72e-152">CommonParameters</span></span>
<span data-ttu-id="1b72e-153">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1b72e-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b72e-154">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1b72e-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b72e-155">輸入</span><span class="sxs-lookup"><span data-stu-id="1b72e-155">INPUTS</span></span>

### <span data-ttu-id="1b72e-156">所有</span><span class="sxs-lookup"><span data-stu-id="1b72e-156">None</span></span>
<span data-ttu-id="1b72e-157">您可以依名稱將輸入輸送至 **SubscriptionName** 屬性，但不能依值。</span><span class="sxs-lookup"><span data-stu-id="1b72e-157">You can pipe input to the **SubscriptionName** property by name, but not by value.</span></span>

## <span data-ttu-id="1b72e-158">輸出</span><span class="sxs-lookup"><span data-stu-id="1b72e-158">OUTPUTS</span></span>

### <span data-ttu-id="1b72e-159">WindowsAzure. 常見. WindowsAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="1b72e-159">Microsoft.WindowsAzure.Commands.Utilities.Common.WindowsAzureSubscription</span></span>

## <span data-ttu-id="1b72e-160">筆記</span><span class="sxs-lookup"><span data-stu-id="1b72e-160">NOTES</span></span>
* <span data-ttu-id="1b72e-161">Get-AzureSubscription 從 **AzureAccount** 和匯 **入 PublishSettingsFile** Cmdlet 建立的訂閱資料檔中取得資料。</span><span class="sxs-lookup"><span data-stu-id="1b72e-161">Get-AzureSubscription gets data from the subscription data file that the **Add-AzureAccount** and **Import-PublishSettingsFile** cmdlets create.</span></span>

## <span data-ttu-id="1b72e-162">相關連結</span><span class="sxs-lookup"><span data-stu-id="1b72e-162">RELATED LINKS</span></span>

[<span data-ttu-id="1b72e-163">附加 AzureAccount</span><span class="sxs-lookup"><span data-stu-id="1b72e-163">Add-AzureAccount</span></span>](./Add-AzureAccount.md)

[<span data-ttu-id="1b72e-164">AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="1b72e-164">Get-AzurePublishSettingsFile</span></span>](./Get-AzurePublishSettingsFile.md)

[<span data-ttu-id="1b72e-165">匯入-AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="1b72e-165">Import-AzurePublishSettingsFile</span></span>](./Import-AzurePublishSettingsFile.md)

[<span data-ttu-id="1b72e-166">移除-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="1b72e-166">Remove-AzureSubscription</span></span>](./Remove-AzureSubscription.md)

[<span data-ttu-id="1b72e-167">Set-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="1b72e-167">Set-AzureSubscription</span></span>](./Set-AzureSubscription.md)


