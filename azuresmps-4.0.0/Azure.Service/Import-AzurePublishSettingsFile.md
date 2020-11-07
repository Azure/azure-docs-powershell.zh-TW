---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 79D64D7C-6671-4F03-8776-70A716F36512
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2bc0525ee7238de421842b74f52f7dd4fa59df1a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967707"
---
# <span data-ttu-id="7c84b-101">Import-AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="7c84b-101">Import-AzurePublishSettingsFile</span></span>

## <span data-ttu-id="7c84b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7c84b-102">SYNOPSIS</span></span>
<span data-ttu-id="7c84b-103">匯入可讓您在 Windows PowerShell 中管理 Azure 帳戶的發佈設定檔。</span><span class="sxs-lookup"><span data-stu-id="7c84b-103">Imports a publish settings file that lets you manage your Azure accounts in Windows PowerShell.</span></span>

## <span data-ttu-id="7c84b-104">句法</span><span class="sxs-lookup"><span data-stu-id="7c84b-104">SYNTAX</span></span>

```
Import-AzurePublishSettingsFile -PublishSettingsFile <String> [-Environment <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="7c84b-105">說明</span><span class="sxs-lookup"><span data-stu-id="7c84b-105">DESCRIPTION</span></span>
<span data-ttu-id="7c84b-106">匯 **入-AzurePublishSettingsFile** Cmdlet 會 ( \*. publishsettings) 中匯入發佈設定檔案，其中包含 Azure 帳戶的相關資訊，並將訂閱資料檔案儲存在您的電腦上。</span><span class="sxs-lookup"><span data-stu-id="7c84b-106">The **Import-AzurePublishSettingsFile** cmdlet imports a publish settings file (\*.publishsettings) that contains information about your Azure accounts and saves a subscription data file on your computer.</span></span>
<span data-ttu-id="7c84b-107">當 Cmdlet 完成時，您可以在 Windows PowerShell 中管理 Azure 帳戶。</span><span class="sxs-lookup"><span data-stu-id="7c84b-107">When the cmdlet completes, you can manage your Azure accounts in Windows PowerShell.</span></span>

<span data-ttu-id="7c84b-108">在執行匯 **入-AzurePublishSettingsFile** 之前，請執行 **AzurePublishSettingsFile** ，這會下載並儲存發佈設定檔案，以便您匯入。</span><span class="sxs-lookup"><span data-stu-id="7c84b-108">Before running **Import-AzurePublishSettingsFile** , run **Get-AzurePublishSettingsFile** , which downloads and saves the publish settings file so you can import it.</span></span>

<span data-ttu-id="7c84b-109">若要讓您的 Azure 帳戶可供 Windows PowerShell 使用，您可以使用發佈設定檔案或 **AzureAccount** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7c84b-109">To make your Azure account available to Windows PowerShell, you can use a publish settings file or the **Add-AzureAccount** cmdlet.</span></span>
<span data-ttu-id="7c84b-110">[發佈設定檔案] 可讓您事先準備會話，讓您能夠以無人參與的方式執行腳本和背景作業。</span><span class="sxs-lookup"><span data-stu-id="7c84b-110">Publish settings files let you prepare the session in advance so you can run scripts and background jobs unattended.</span></span>
<span data-ttu-id="7c84b-111">不過，並非所有的服務都支援發佈設定檔案。</span><span class="sxs-lookup"><span data-stu-id="7c84b-111">However, not all services support publish settings files.</span></span>
<span data-ttu-id="7c84b-112">例如， **AzureResourceManager** 模組不支援發佈設定檔案。</span><span class="sxs-lookup"><span data-stu-id="7c84b-112">For example, the **AzureResourceManager** module does not support publish settings files.</span></span>

<span data-ttu-id="7c84b-113">**安全性注意事項：** 發佈設定檔案包含已編碼但未加密的管理憑證。</span><span class="sxs-lookup"><span data-stu-id="7c84b-113">**Security Note:** Publish settings files contain a management certificate that is encoded, but not encrypted.</span></span>
<span data-ttu-id="7c84b-114">如果惡意使用者存取您的發佈設定檔案，他們可能可以編輯、建立及刪除您的 Azure 服務。</span><span class="sxs-lookup"><span data-stu-id="7c84b-114">If  malicious users access your publish settings file,  they might be able to edit, create, and delete your Azure services.</span></span>
<span data-ttu-id="7c84b-115">為安全性最佳做法，請將檔案儲存到 [下載] 或 [檔] 資料夾中的某個位置，然後在使用匯 **入 AzurePublishSettingsFile** Cmdlet 匯入設定之後刪除該位置。</span><span class="sxs-lookup"><span data-stu-id="7c84b-115">As a security best practice, save the file to a location in your Downloads or Documents folder and then delete it after using **Import-AzurePublishSettingsFile** cmdlet to import the settings.</span></span>

## <span data-ttu-id="7c84b-116">示例</span><span class="sxs-lookup"><span data-stu-id="7c84b-116">EXAMPLES</span></span>

### <span data-ttu-id="7c84b-117">範例1：匯入檔案</span><span class="sxs-lookup"><span data-stu-id="7c84b-117">Example 1: Import a file</span></span>
```
PS C:\> Import-AzurePublishSettingsFile -PublishSettingsFile C:\Temp\MyAccount.publishsettings
```

<span data-ttu-id="7c84b-118">這個命令會將 [C:\Temp\MyAccount.publishsettings] 檔案匯入。</span><span class="sxs-lookup"><span data-stu-id="7c84b-118">This command imports the "C:\Temp\MyAccount.publishsettings" file.</span></span>

## <span data-ttu-id="7c84b-119">參數</span><span class="sxs-lookup"><span data-stu-id="7c84b-119">PARAMETERS</span></span>

### <span data-ttu-id="7c84b-120">-環境</span><span class="sxs-lookup"><span data-stu-id="7c84b-120">-Environment</span></span>
<span data-ttu-id="7c84b-121">指定 Azure 環境。</span><span class="sxs-lookup"><span data-stu-id="7c84b-121">Specifies an Azure environment.</span></span>

<span data-ttu-id="7c84b-122">Azure 環境是獨立部署的 Microsoft Azure，例如針對全域 Azure 的 AzureCloud，以及由中國由世紀運營之 AzureChinaCloud 的 Azure。</span><span class="sxs-lookup"><span data-stu-id="7c84b-122">An Azure environment an independent deployment of Microsoft Azure, such as AzureCloud for global Azure and AzureChinaCloud for Azure operated by 21Vianet in China.</span></span>
<span data-ttu-id="7c84b-123">您也可以使用 Azure Pack 和 WAPack Cmdlet，建立內部部署的 Azure 環境。</span><span class="sxs-lookup"><span data-stu-id="7c84b-123">You can also create on-premises Azure environments by using Azure Pack and the WAPack cmdlets.</span></span>
<span data-ttu-id="7c84b-124">如需詳細資訊，請參閱 [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  (https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="7c84b-124">For more information, see [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  (https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c84b-125">-設定檔</span><span class="sxs-lookup"><span data-stu-id="7c84b-125">-Profile</span></span>
<span data-ttu-id="7c84b-126">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="7c84b-126">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="7c84b-127">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="7c84b-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7c84b-128">-PublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="7c84b-128">-PublishSettingsFile</span></span>
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

### <span data-ttu-id="7c84b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c84b-129">CommonParameters</span></span>
<span data-ttu-id="7c84b-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7c84b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c84b-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7c84b-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c84b-132">輸入</span><span class="sxs-lookup"><span data-stu-id="7c84b-132">INPUTS</span></span>

### <span data-ttu-id="7c84b-133">所有</span><span class="sxs-lookup"><span data-stu-id="7c84b-133">None</span></span>
<span data-ttu-id="7c84b-134">您可以透過屬性名稱（而不是依值），將輸入管到這個 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7c84b-134">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="7c84b-135">輸出</span><span class="sxs-lookup"><span data-stu-id="7c84b-135">OUTPUTS</span></span>

### <span data-ttu-id="7c84b-136">所有</span><span class="sxs-lookup"><span data-stu-id="7c84b-136">None</span></span>
<span data-ttu-id="7c84b-137">這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="7c84b-137">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="7c84b-138">筆記</span><span class="sxs-lookup"><span data-stu-id="7c84b-138">NOTES</span></span>
* <span data-ttu-id="7c84b-139">"發佈設定檔案" 是副檔名為 publishsettings 的 XML 檔案。</span><span class="sxs-lookup"><span data-stu-id="7c84b-139">A "publish settings file" is an XML file with a .publishsettings file name extension.</span></span> <span data-ttu-id="7c84b-140">檔案包含為您的 Azure 訂閱提供管理認證的編碼證書。</span><span class="sxs-lookup"><span data-stu-id="7c84b-140">The file contains an encoded certificate that provides management credentials for your Azure subscriptions.</span></span> <span data-ttu-id="7c84b-141">匯入此檔案之後，請將其刪除以避免安全性風險。</span><span class="sxs-lookup"><span data-stu-id="7c84b-141">After you import this file, delete it to avoid security risks.</span></span>
* <span data-ttu-id="7c84b-142">「訂閱資料檔」是可在您的電腦上安全儲存的 XML 檔案。</span><span class="sxs-lookup"><span data-stu-id="7c84b-142">A "subscription data file" is an XML file that can be saved on your computer safely.</span></span> <span data-ttu-id="7c84b-143">根據預設，它會儲存在您的漫遊使用者設定檔中 ($home/AppData/Roaming) ]。</span><span class="sxs-lookup"><span data-stu-id="7c84b-143">By default, it's saved in your roaming user profile ($home/AppData/Roaming).</span></span>

## <span data-ttu-id="7c84b-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="7c84b-144">RELATED LINKS</span></span>

[<span data-ttu-id="7c84b-145">如何安裝和設定 Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="7c84b-145">How to Install and Configure Azure PowerShell</span></span>](https://azure.microsoft.com/documentation/articles/install-configure-powershell/)

[<span data-ttu-id="7c84b-146">附加 AzureAccount</span><span class="sxs-lookup"><span data-stu-id="7c84b-146">Add-AzureAccount</span></span>](./Add-AzureAccount.md)

[<span data-ttu-id="7c84b-147">AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="7c84b-147">Get-AzurePublishSettingsFile</span></span>](./Get-AzurePublishSettingsFile.md)


