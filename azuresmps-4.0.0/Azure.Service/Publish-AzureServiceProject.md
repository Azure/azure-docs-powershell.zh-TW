---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: CF7E7C62-88FC-48CA-940F-9A6C7442BEF2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8166cd3faa951171dd3ac865b17b8a03bcefdd45
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967329"
---
# <span data-ttu-id="86b0c-101">Publish-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="86b0c-101">Publish-AzureServiceProject</span></span>

## <span data-ttu-id="86b0c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="86b0c-102">SYNOPSIS</span></span>
<span data-ttu-id="86b0c-103">將目前的服務發佈到 Windows Azure。</span><span class="sxs-lookup"><span data-stu-id="86b0c-103">Publish the current service to Windows Azure.</span></span>

## <span data-ttu-id="86b0c-104">句法</span><span class="sxs-lookup"><span data-stu-id="86b0c-104">SYNTAX</span></span>

### <span data-ttu-id="86b0c-105">PublishFromServiceDefinition (預設) </span><span class="sxs-lookup"><span data-stu-id="86b0c-105">PublishFromServiceDefinition (Default)</span></span>
```
Publish-AzureServiceProject [-ServiceName <String>] [-StorageAccountName <String>] [-Location <String>]
 [-Slot <String>] [-Launch] [-AffinityGroup <String>] [-DeploymentName <String>] [-ForceUpgrade]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="86b0c-106">PublishFromPackage</span><span class="sxs-lookup"><span data-stu-id="86b0c-106">PublishFromPackage</span></span>
```
Publish-AzureServiceProject [-Package <String>] -Configuration <String> [-StorageAccountName <String>]
 [-Location <String>] [-Slot <String>] [-Launch] [-AffinityGroup <String>] [-DeploymentName <String>]
 [-ForceUpgrade] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="86b0c-107">說明</span><span class="sxs-lookup"><span data-stu-id="86b0c-107">DESCRIPTION</span></span>
<span data-ttu-id="86b0c-108">本主題描述 Microsoft Azure PowerShell 模組的0.8.10 版本中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="86b0c-108">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="86b0c-109">若要取得您正在使用的模組版本，請在 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。</span><span class="sxs-lookup"><span data-stu-id="86b0c-109">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="86b0c-110">**AzureServiceProject** Cmdlet 會將目前的服務發佈到雲端。</span><span class="sxs-lookup"><span data-stu-id="86b0c-110">The **Publish-AzureServiceProject** cmdlet publishes the current service to the cloud.</span></span>
<span data-ttu-id="86b0c-111">您可以在命令列上指定發佈設定 (例如 **訂閱** 、 **StorageAccountName** 、 **位置** 、 **槽** ) ，或透過 **AzureServiceProject** Cmdlet 在本機設定中指定。</span><span class="sxs-lookup"><span data-stu-id="86b0c-111">You can specify publishing configuration (such as **Subscription** , **StorageAccountName** , **Location** , **Slot** ) on the command line, or in local settings through the **Set-AzureServiceProject** cmdlet.</span></span>

## <span data-ttu-id="86b0c-112">示例</span><span class="sxs-lookup"><span data-stu-id="86b0c-112">EXAMPLES</span></span>

### <span data-ttu-id="86b0c-113">範例1：發佈含預設值的服務專案</span><span class="sxs-lookup"><span data-stu-id="86b0c-113">Example 1: Publish a service project with default values</span></span>
```
PS C:\> Publish-AzureServiceProject
```

<span data-ttu-id="86b0c-114">這個範例會使用目前的服務設定和目前的 Azure 發佈設定檔，發佈目前的服務。</span><span class="sxs-lookup"><span data-stu-id="86b0c-114">This example publishes the current service, using the current service settings and the current Azure publish profile.</span></span>

### <span data-ttu-id="86b0c-115">範例2：建立部署套件</span><span class="sxs-lookup"><span data-stu-id="86b0c-115">Example 2: Create a deployment package</span></span>
```
PS C:\> Publish-AzureServiceProject -PackageOnly
```

<span data-ttu-id="86b0c-116">這個範例會在 service 目錄中建立部署套件 () 檔案，但不會發佈到 Windows Azure。</span><span class="sxs-lookup"><span data-stu-id="86b0c-116">This example creates a deployment package (.cspkg) file in the service directory and does not publish to Windows Azure.</span></span>

## <span data-ttu-id="86b0c-117">參數</span><span class="sxs-lookup"><span data-stu-id="86b0c-117">PARAMETERS</span></span>

### <span data-ttu-id="86b0c-118">-AffinityGroup</span><span class="sxs-lookup"><span data-stu-id="86b0c-118">-AffinityGroup</span></span>
<span data-ttu-id="86b0c-119">指定您希望服務使用的地緣群組。</span><span class="sxs-lookup"><span data-stu-id="86b0c-119">Specifies the affinity group that you want the service to use.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86b0c-120">-配置</span><span class="sxs-lookup"><span data-stu-id="86b0c-120">-Configuration</span></span>
<span data-ttu-id="86b0c-121">指定服務設定檔。</span><span class="sxs-lookup"><span data-stu-id="86b0c-121">Specifies the service configuration file.</span></span>
<span data-ttu-id="86b0c-122">如果您指定此參數，請指定 *Package* 參數。</span><span class="sxs-lookup"><span data-stu-id="86b0c-122">If you specify this parameter, specify the *Package* parameter.</span></span>

```yaml
Type: String
Parameter Sets: PublishFromPackage
Aliases: cc

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86b0c-123">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="86b0c-123">-DeploymentName</span></span>
<span data-ttu-id="86b0c-124">指定部署名稱。</span><span class="sxs-lookup"><span data-stu-id="86b0c-124">Specifies the deployment name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: dn

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86b0c-125">-ForceUpgrade</span><span class="sxs-lookup"><span data-stu-id="86b0c-125">-ForceUpgrade</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: f

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86b0c-126">-啟動</span><span class="sxs-lookup"><span data-stu-id="86b0c-126">-Launch</span></span>
<span data-ttu-id="86b0c-127">開啟瀏覽器視窗，讓您在部署之後就能查看應用程式。</span><span class="sxs-lookup"><span data-stu-id="86b0c-127">Opens a browser window so you can view the application after it is deployed.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: ln

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86b0c-128">-位置</span><span class="sxs-lookup"><span data-stu-id="86b0c-128">-Location</span></span>
<span data-ttu-id="86b0c-129">將託管應用程式的地區。</span><span class="sxs-lookup"><span data-stu-id="86b0c-129">The region in which the application will be hosted.</span></span>
<span data-ttu-id="86b0c-130">可能的值包括：</span><span class="sxs-lookup"><span data-stu-id="86b0c-130">Possible values are:</span></span> 
  
- <span data-ttu-id="86b0c-131">亞洲任何地方</span><span class="sxs-lookup"><span data-stu-id="86b0c-131">Anywhere Asia</span></span>
- <span data-ttu-id="86b0c-132">歐洲任何地方</span><span class="sxs-lookup"><span data-stu-id="86b0c-132">Anywhere Europe</span></span>
- <span data-ttu-id="86b0c-133">美國任何地方</span><span class="sxs-lookup"><span data-stu-id="86b0c-133">Anywhere US</span></span>
- <span data-ttu-id="86b0c-134">東亞</span><span class="sxs-lookup"><span data-stu-id="86b0c-134">East Asia</span></span>
- <span data-ttu-id="86b0c-135">東美國</span><span class="sxs-lookup"><span data-stu-id="86b0c-135">East US</span></span>
- <span data-ttu-id="86b0c-136">美國中北部</span><span class="sxs-lookup"><span data-stu-id="86b0c-136">North Central US</span></span>
- <span data-ttu-id="86b0c-137">北歐</span><span class="sxs-lookup"><span data-stu-id="86b0c-137">North Europe</span></span>
- <span data-ttu-id="86b0c-138">美國中南部</span><span class="sxs-lookup"><span data-stu-id="86b0c-138">South Central US</span></span>
- <span data-ttu-id="86b0c-139">東南亞</span><span class="sxs-lookup"><span data-stu-id="86b0c-139">Southeast Asia</span></span>
- <span data-ttu-id="86b0c-140">西歐</span><span class="sxs-lookup"><span data-stu-id="86b0c-140">West Europe</span></span>
- <span data-ttu-id="86b0c-141">美國西部</span><span class="sxs-lookup"><span data-stu-id="86b0c-141">West US</span></span>
 
<span data-ttu-id="86b0c-142">如果未指定位置，則會使用在最後一次呼叫 **AzureServiceProject** 中指定的位置。</span><span class="sxs-lookup"><span data-stu-id="86b0c-142">If no Location is specified, the location specified in the last call to **Set-AzureServiceProject** will be used.</span></span> <span data-ttu-id="86b0c-143">如果未指定位置，位置將會從「中北部」和「中南部 US」位置隨機選取。</span><span class="sxs-lookup"><span data-stu-id="86b0c-143">If no Location was ever specified, the Location will be randomly chosen from 'North Central US' and 'South Central US' locations.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: l

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86b0c-144">-套件</span><span class="sxs-lookup"><span data-stu-id="86b0c-144">-Package</span></span>
<span data-ttu-id="86b0c-145">指定要部署的套件檔案。</span><span class="sxs-lookup"><span data-stu-id="86b0c-145">Specifies the package file to deploy.</span></span>
<span data-ttu-id="86b0c-146">指定副檔名為 cspkg 的本機檔案，或是包含該套件之 blob 的 URI。</span><span class="sxs-lookup"><span data-stu-id="86b0c-146">Specify either a local file that has the .cspkg file name extension or a URI of a blob that contains the package.</span></span>
<span data-ttu-id="86b0c-147">如果您指定此參數，請勿指定 *ServiceName* 參數。</span><span class="sxs-lookup"><span data-stu-id="86b0c-147">If you specify this parameter, do not specify the *ServiceName* parameter.</span></span>

```yaml
Type: String
Parameter Sets: PublishFromPackage
Aliases: sp

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86b0c-148">-設定檔</span><span class="sxs-lookup"><span data-stu-id="86b0c-148">-Profile</span></span>
<span data-ttu-id="86b0c-149">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="86b0c-149">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="86b0c-150">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="86b0c-150">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="86b0c-151">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="86b0c-151">-ServiceName</span></span>
<span data-ttu-id="86b0c-152">指定發佈至 Windows Azure 時要用於服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="86b0c-152">Specifies the name to be used for the service when publishing to Windows Azure.</span></span>
<span data-ttu-id="86b0c-153">名稱會判斷 cloudapp.net 子域中的部分標籤，用來在 Windows (Azure 中託管（cloudapp.net **) ）時** 用來處理服務。</span><span class="sxs-lookup"><span data-stu-id="86b0c-153">The name determines part of the label in the cloudapp.net subdomain that is used to address the service when hosted in Windows Azure (that is, **name**.cloudapp.net).</span></span>
<span data-ttu-id="86b0c-154">發佈服務時指定的任何名稱會覆寫建立服務時所提供的名稱。</span><span class="sxs-lookup"><span data-stu-id="86b0c-154">Any name specified while publishing the service overrides the name given when the service was created.</span></span>
<span data-ttu-id="86b0c-155"> (查看 **新的 AzureServiceProject** Cmdlet) 。</span><span class="sxs-lookup"><span data-stu-id="86b0c-155">(See the **New-AzureServiceProject** cmdlet).</span></span>

```yaml
Type: String
Parameter Sets: PublishFromServiceDefinition
Aliases: sv

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86b0c-156">-槽</span><span class="sxs-lookup"><span data-stu-id="86b0c-156">-Slot</span></span>
<span data-ttu-id="86b0c-157">要用於此服務的部署槽位。</span><span class="sxs-lookup"><span data-stu-id="86b0c-157">The deployment slot to be used for this service.</span></span>
<span data-ttu-id="86b0c-158">可能的值為「分段」和「生產」。</span><span class="sxs-lookup"><span data-stu-id="86b0c-158">Possible values are 'Staging' and 'Production'.</span></span>
<span data-ttu-id="86b0c-159">如果未指定任何槽，則會使用在最後一個 Set-AzureDeploymentSlot 呼叫中提供的槽。</span><span class="sxs-lookup"><span data-stu-id="86b0c-159">If no slot is specified, the slot provided in the last call to Set-AzureDeploymentSlot is used.</span></span>
<span data-ttu-id="86b0c-160">如果沒有指定任何槽，則會使用「生產」槽。</span><span class="sxs-lookup"><span data-stu-id="86b0c-160">If no slot has ever been specified, the 'Production' slot is used.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: sl

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86b0c-161">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="86b0c-161">-StorageAccountName</span></span>
<span data-ttu-id="86b0c-162">指定發佈服務時要使用的 Windows Azure 儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="86b0c-162">Specifies the Windows Azure storage account name to be used while publishing the service.</span></span>
<span data-ttu-id="86b0c-163">在發行服務之前，不會使用這個值。</span><span class="sxs-lookup"><span data-stu-id="86b0c-163">This value is not used until the service is published.</span></span>
<span data-ttu-id="86b0c-164">如果未指定此參數，則會從最後一個 [ **設定 AzureServiceProject** ] 命令取得值。</span><span class="sxs-lookup"><span data-stu-id="86b0c-164">When this parameter is not specified, the value is obtained from the last **Set-AzureServiceProject** command.</span></span>
<span data-ttu-id="86b0c-165">如果您從未指定過儲存空間，就會使用符合服務名稱的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="86b0c-165">If no storage account was ever specified, a storage account matching the name of the service will be used.</span></span>
<span data-ttu-id="86b0c-166">如果不存在這樣的儲存帳戶，此 Cmdlet 會嘗試建立新帳戶。</span><span class="sxs-lookup"><span data-stu-id="86b0c-166">If no such storage account exists, the cmdlet attempts to create a new one.</span></span>
<span data-ttu-id="86b0c-167">不過，如果在其他訂閱中存在與服務名稱相符的儲存空間帳戶，嘗試可能會失敗。</span><span class="sxs-lookup"><span data-stu-id="86b0c-167">However, the attempt may fail if a storage account matching the service name exists in another subscription.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: st

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86b0c-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86b0c-168">CommonParameters</span></span>
<span data-ttu-id="86b0c-169">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="86b0c-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86b0c-170">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="86b0c-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86b0c-171">輸入</span><span class="sxs-lookup"><span data-stu-id="86b0c-171">INPUTS</span></span>

## <span data-ttu-id="86b0c-172">輸出</span><span class="sxs-lookup"><span data-stu-id="86b0c-172">OUTPUTS</span></span>

## <span data-ttu-id="86b0c-173">筆記</span><span class="sxs-lookup"><span data-stu-id="86b0c-173">NOTES</span></span>

## <span data-ttu-id="86b0c-174">相關連結</span><span class="sxs-lookup"><span data-stu-id="86b0c-174">RELATED LINKS</span></span>

[<span data-ttu-id="86b0c-175">Enable-AzureServiceProjectRemoteDesktop</span><span class="sxs-lookup"><span data-stu-id="86b0c-175">Enable-AzureServiceProjectRemoteDesktop</span></span>](./Enable-AzureServiceProjectRemoteDesktop.md)

[<span data-ttu-id="86b0c-176">Set-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="86b0c-176">Set-AzureServiceProject</span></span>](./Set-AzureServiceProject.md)


