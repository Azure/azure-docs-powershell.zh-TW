---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: A5419F76-B85E-445D-84EA-CC695B175C8D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1364cf1bbec1fdca2a8c9901556d38de0b620358
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967079"
---
# <span data-ttu-id="3c4d6-101">Get-AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="3c4d6-101">Get-AzurePublishSettingsFile</span></span>

## <span data-ttu-id="3c4d6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3c4d6-102">SYNOPSIS</span></span>
<span data-ttu-id="3c4d6-103">下載 Azure 訂閱的發佈設定檔案。</span><span class="sxs-lookup"><span data-stu-id="3c4d6-103">Downloads the publish settings file for an Azure subscription.</span></span>

## <span data-ttu-id="3c4d6-104">句法</span><span class="sxs-lookup"><span data-stu-id="3c4d6-104">SYNTAX</span></span>

```
Get-AzurePublishSettingsFile [-Environment <String>] [-Realm <String>] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="3c4d6-105">說明</span><span class="sxs-lookup"><span data-stu-id="3c4d6-105">DESCRIPTION</span></span>
<span data-ttu-id="3c4d6-106">**AzurePublishSettingsFile** Cmdlet 會在您的帳戶中下載訂閱的發佈設定檔案。</span><span class="sxs-lookup"><span data-stu-id="3c4d6-106">The **Get-AzurePublishSettingsFile** cmdlet downloads a publish settings file for a subscription in your account.</span></span>
<span data-ttu-id="3c4d6-107">當命令完成時，您可以使用 **PublishSettingsFile** Cmdlet，將檔案中的設定設為可供 Windows PowerShell 使用。</span><span class="sxs-lookup"><span data-stu-id="3c4d6-107">When the command completes, you can use the **Import-PublishSettingsFile** cmdlet to make the settings in the file available to Windows PowerShell.</span></span>

<span data-ttu-id="3c4d6-108">若要讓您的 Azure 帳戶可供 Windows PowerShell 使用，您可以使用發佈設定檔案或 **AzureAccount** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3c4d6-108">To make your Azure account available to Windows PowerShell, you can use a publish settings file or the **Add-AzureAccount** cmdlet.</span></span>
<span data-ttu-id="3c4d6-109">[發佈設定檔案] 可讓您事先準備會話，讓您能夠以無人參與的方式執行腳本和背景作業。</span><span class="sxs-lookup"><span data-stu-id="3c4d6-109">Publish settings files let you prepare the session in advance so you can run scripts and background jobs unattended.</span></span>
<span data-ttu-id="3c4d6-110">不過，並非所有的服務都支援發佈設定檔案。</span><span class="sxs-lookup"><span data-stu-id="3c4d6-110">However, not all services support publish settings files.</span></span>
<span data-ttu-id="3c4d6-111">例如， **AzureResourceManager** 模組不支援發佈設定檔案。</span><span class="sxs-lookup"><span data-stu-id="3c4d6-111">For example, the **AzureResourceManager** module does not support publish settings files.</span></span>

<span data-ttu-id="3c4d6-112">當您執行 **AzurePublishSettingsFile** 時，會開啟您的預設瀏覽器，並提示您登入您的 Azure 帳戶、選取訂閱，然後選取發佈設定檔的檔案系統位置。</span><span class="sxs-lookup"><span data-stu-id="3c4d6-112">When you run **Get-AzurePublishSettingsFile** , it opens your default browser and prompts you to sign into your Azure account, select a subscription, and select a file system location for the publish settings file.</span></span>
<span data-ttu-id="3c4d6-113">接著，它會將您訂閱的發佈設定檔案下載到您選取的檔案中。</span><span class="sxs-lookup"><span data-stu-id="3c4d6-113">Then, it downloads the publish settings file for your subscription into the file that you selected.</span></span>

<span data-ttu-id="3c4d6-114">"發佈設定檔案" 是副檔名為 publishsettings 的 XML 檔案。</span><span class="sxs-lookup"><span data-stu-id="3c4d6-114">A "publish settings file" is an XML file with a .publishsettings file name extension.</span></span>
<span data-ttu-id="3c4d6-115">檔案包含為您的 Azure 訂閱提供管理認證的編碼證書。</span><span class="sxs-lookup"><span data-stu-id="3c4d6-115">The file contains an encoded certificate that provides management credentials for your Azure subscriptions.</span></span>

<span data-ttu-id="3c4d6-116">**安全性注意事項：** 發佈設定檔案包含用來管理 Azure 訂閱與服務的認證。</span><span class="sxs-lookup"><span data-stu-id="3c4d6-116">**Security Note:** Publish settings files contains credentials that are used to administer your Azure subscriptions and services.</span></span>
<span data-ttu-id="3c4d6-117">如果惡意使用者存取您的發佈設定檔案，他們就可以編輯、建立及刪除您的 Azure 服務。</span><span class="sxs-lookup"><span data-stu-id="3c4d6-117">If  malicious users access your publish settings file,  they can edit, create, and delete your Azure services.</span></span>
<span data-ttu-id="3c4d6-118">為安全性最佳做法，請將檔案儲存到 [下載] 或 [檔] 資料夾中的某個位置，然後在使用匯 **入 AzurePublishSettingsFile** Cmdlet 匯入設定之後刪除該位置。</span><span class="sxs-lookup"><span data-stu-id="3c4d6-118">As a security best practice, save the file to a location in your Downloads or Documents folder and then delete it after using **Import-AzurePublishSettingsFile** cmdlet to import the settings.</span></span>

<span data-ttu-id="3c4d6-119">本主題描述 Microsoft Azure PowerShell 模組的0.8.10 版本中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3c4d6-119">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="3c4d6-120">若要取得您正在使用的模組版本，請在 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。</span><span class="sxs-lookup"><span data-stu-id="3c4d6-120">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="3c4d6-121">示例</span><span class="sxs-lookup"><span data-stu-id="3c4d6-121">EXAMPLES</span></span>

### <span data-ttu-id="3c4d6-122">範例1：下載發佈設定檔</span><span class="sxs-lookup"><span data-stu-id="3c4d6-122">Example 1: Download a publish settings file</span></span>
```
PS C:\> Get-AzurePublishSettingsFile
```

<span data-ttu-id="3c4d6-123">這個命令會開啟您的預設瀏覽器、連線到您的 Windows Azure 帳戶，然後下載您帳戶的 publishsettings 檔案。</span><span class="sxs-lookup"><span data-stu-id="3c4d6-123">This command opens your default browser, connects to your Windows Azure account, and then downloads the .publishsettings file for your account.</span></span>

### <span data-ttu-id="3c4d6-124">範例2：指定領域</span><span class="sxs-lookup"><span data-stu-id="3c4d6-124">Example 2: Specify a realm</span></span>
```
PS C:\> Get-AzurePublishSettingsFile -Realm contoso.com -Passthru
```

<span data-ttu-id="3c4d6-125">這個命令會下載 contoso.com 網域中帳戶的發佈設定檔案。</span><span class="sxs-lookup"><span data-stu-id="3c4d6-125">This command downloads the publish settings file for an account in the contoso.com domain.</span></span>
<span data-ttu-id="3c4d6-126">當您使用組織帳戶（而非 Microsoft 帳戶）登入 Azure 時，請使用帶有 **Realm** 參數的命令。</span><span class="sxs-lookup"><span data-stu-id="3c4d6-126">Use a command with the **Realm** parameter when you sign into Azure with an organizational account, instead of a Microsoft account.</span></span>

## <span data-ttu-id="3c4d6-127">參數</span><span class="sxs-lookup"><span data-stu-id="3c4d6-127">PARAMETERS</span></span>

### <span data-ttu-id="3c4d6-128">-環境</span><span class="sxs-lookup"><span data-stu-id="3c4d6-128">-Environment</span></span>
<span data-ttu-id="3c4d6-129">指定 Azure 環境。</span><span class="sxs-lookup"><span data-stu-id="3c4d6-129">Specifies an Azure environment.</span></span>

<span data-ttu-id="3c4d6-130">Azure 環境是獨立部署的 Microsoft Azure，例如針對全域 Azure 的 AzureCloud，以及由中國由世紀運營之 AzureChinaCloud 的 Azure。</span><span class="sxs-lookup"><span data-stu-id="3c4d6-130">An Azure environment an independent deployment of Microsoft Azure, such as AzureCloud for global Azure and AzureChinaCloud for Azure operated by 21Vianet in China.</span></span>
<span data-ttu-id="3c4d6-131">您也可以使用 Azure Pack 和 WAPack Cmdlet，建立內部部署的 Azure 環境。</span><span class="sxs-lookup"><span data-stu-id="3c4d6-131">You can also create on-premises Azure environments by using Azure Pack and the WAPack cmdlets.</span></span>
<span data-ttu-id="3c4d6-132">如需詳細資訊，請參閱 [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  (https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="3c4d6-132">For more information, see [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  (https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx).</span></span>

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

### <span data-ttu-id="3c4d6-133">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3c4d6-133">-PassThru</span></span>
<span data-ttu-id="3c4d6-134">如果命令成功，則傳回 $True，且 $False 失敗。</span><span class="sxs-lookup"><span data-stu-id="3c4d6-134">Returns $True if the command succeeds and $False if it fails.</span></span>
<span data-ttu-id="3c4d6-135">根據預設，這個 Cmdlet 不會傳回任何輸出。</span><span class="sxs-lookup"><span data-stu-id="3c4d6-135">By default, this cmdlet does not return any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c4d6-136">-設定檔</span><span class="sxs-lookup"><span data-stu-id="3c4d6-136">-Profile</span></span>
<span data-ttu-id="3c4d6-137">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="3c4d6-137">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="3c4d6-138">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="3c4d6-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3c4d6-139">-領域</span><span class="sxs-lookup"><span data-stu-id="3c4d6-139">-Realm</span></span>
<span data-ttu-id="3c4d6-140">指定組織識別碼中的組織。</span><span class="sxs-lookup"><span data-stu-id="3c4d6-140">Specifies the organization in an organizational ID.</span></span>
<span data-ttu-id="3c4d6-141">例如，如果您登入 [Azure as] admin@contoso.com ，則會 contoso.com [ **Realm** ] 參數的值。</span><span class="sxs-lookup"><span data-stu-id="3c4d6-141">For example, if you sign into Azure as admin@contoso.com, the value of the **Realm** parameter is contoso.com.</span></span>
<span data-ttu-id="3c4d6-142">當您使用組織識別碼登入 Azure 入口網站時，請使用此參數。</span><span class="sxs-lookup"><span data-stu-id="3c4d6-142">Use this parameter when you use an organizational ID to sign into the Azure portal.</span></span>
<span data-ttu-id="3c4d6-143">如果您使用的是 Microsoft 帳戶，例如 outlook.com 或 live.com 帳戶，則不需要此參數。</span><span class="sxs-lookup"><span data-stu-id="3c4d6-143">This parameter is not required when you use a Microsoft account, such as an outlook.com or live.com account.</span></span>

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

### <span data-ttu-id="3c4d6-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c4d6-144">CommonParameters</span></span>
<span data-ttu-id="3c4d6-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3c4d6-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c4d6-146">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3c4d6-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c4d6-147">輸入</span><span class="sxs-lookup"><span data-stu-id="3c4d6-147">INPUTS</span></span>

### <span data-ttu-id="3c4d6-148">所有</span><span class="sxs-lookup"><span data-stu-id="3c4d6-148">None</span></span>
<span data-ttu-id="3c4d6-149">您可以透過屬性名稱（而不是依值），將輸入管到這個 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3c4d6-149">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="3c4d6-150">輸出</span><span class="sxs-lookup"><span data-stu-id="3c4d6-150">OUTPUTS</span></span>

### <span data-ttu-id="3c4d6-151">None 或 System.object</span><span class="sxs-lookup"><span data-stu-id="3c4d6-151">None or System.Boolean</span></span>
<span data-ttu-id="3c4d6-152">當您使用 *PassThru* 參數時，這個 Cmdlet 會傳回布林值。</span><span class="sxs-lookup"><span data-stu-id="3c4d6-152">When you use the *PassThru* parameter, this cmdlet returns a Boolean value.</span></span>
<span data-ttu-id="3c4d6-153">否則，此 Cmdlet 不會傳回任何輸出</span><span class="sxs-lookup"><span data-stu-id="3c4d6-153">Otherwise, this cmdlet does not return any output</span></span>

## <span data-ttu-id="3c4d6-154">筆記</span><span class="sxs-lookup"><span data-stu-id="3c4d6-154">NOTES</span></span>

## <span data-ttu-id="3c4d6-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="3c4d6-155">RELATED LINKS</span></span>

[<span data-ttu-id="3c4d6-156">附加 AzureAccount</span><span class="sxs-lookup"><span data-stu-id="3c4d6-156">Add-AzureAccount</span></span>](./Add-AzureAccount.md)

[<span data-ttu-id="3c4d6-157">匯入-AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="3c4d6-157">Import-AzurePublishSettingsFile</span></span>](./Import-AzurePublishSettingsFile.md)


