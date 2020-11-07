---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: D6D4E733-31AE-4ABE-8C78-583EC48C56B8
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/new-Azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/New-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/New-AzWebApp.md
ms.openlocfilehash: ec5f9cf60025e6b35248b2e7f8058040b404ec42
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794980"
---
# <span data-ttu-id="b93f0-101">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="b93f0-101">New-AzWebApp</span></span>

## <span data-ttu-id="b93f0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b93f0-102">SYNOPSIS</span></span>
<span data-ttu-id="b93f0-103">建立 Azure Web App。</span><span class="sxs-lookup"><span data-stu-id="b93f0-103">Creates an Azure Web App.</span></span>

## <span data-ttu-id="b93f0-104">句法</span><span class="sxs-lookup"><span data-stu-id="b93f0-104">SYNTAX</span></span>

### <span data-ttu-id="b93f0-105">SimpleParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="b93f0-105">SimpleParameterSet (Default)</span></span>
```
New-AzWebApp [[-ResourceGroupName] <String>] [-Name] <String> [[-Location] <String>]
 [[-AppServicePlan] <String>] [-AsJob] [-GitRepositoryPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b93f0-106">WebAppParameterSet</span><span class="sxs-lookup"><span data-stu-id="b93f0-106">WebAppParameterSet</span></span>
```
New-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-AppServicePlan] <String>] [-SourceWebApp] <Site> [[-TrafficManagerProfile] <String>] [-IgnoreSourceControl]
 [-IgnoreCustomHostNames] [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>]
 [[-AseResourceGroupName] <String>] [-IncludeSourceWebAppSlots] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b93f0-107">說明</span><span class="sxs-lookup"><span data-stu-id="b93f0-107">DESCRIPTION</span></span>
<span data-ttu-id="b93f0-108">**AzWebApp** Cmdlet 會在指定的資源群組中，使用指定的應用程式服務方案和資料中心來建立 Azure Web App。</span><span class="sxs-lookup"><span data-stu-id="b93f0-108">The **New-AzWebApp** cmdlet creates an Azure Web App in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="b93f0-109">示例</span><span class="sxs-lookup"><span data-stu-id="b93f0-109">EXAMPLES</span></span>

### <span data-ttu-id="b93f0-110">範例1：建立 Web 應用程式</span><span class="sxs-lookup"><span data-stu-id="b93f0-110">Example 1: Create a Web App</span></span>
```
PS C:\>New-AzWebApp -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -Location "West US" -AppServicePlan "ContosoServicePlan"
```

<span data-ttu-id="b93f0-111">這個命令會在資料中心的名為「預設-Web-WestUS」的現有資源群組中，建立名為 ContosoSite 的 Azure Web App。</span><span class="sxs-lookup"><span data-stu-id="b93f0-111">This command creates an Azure Web App named ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="b93f0-112">此命令使用名為 ContosoServicePlan 的現有應用程式服務方案。</span><span class="sxs-lookup"><span data-stu-id="b93f0-112">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="b93f0-113">參數</span><span class="sxs-lookup"><span data-stu-id="b93f0-113">PARAMETERS</span></span>

### <span data-ttu-id="b93f0-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="b93f0-114">-AppServicePlan</span></span>
<span data-ttu-id="b93f0-115">App 服務方案名稱</span><span class="sxs-lookup"><span data-stu-id="b93f0-115">App Service Plan Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b93f0-116">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="b93f0-116">-AppSettingsOverrides</span></span>
<span data-ttu-id="b93f0-117">應用程式設定會覆寫 HashTable</span><span class="sxs-lookup"><span data-stu-id="b93f0-117">App Settings Overrides HashTable</span></span>

```yaml
Type: Hashtable
Parameter Sets: WebAppParameterSet
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b93f0-118">-AseName</span><span class="sxs-lookup"><span data-stu-id="b93f0-118">-AseName</span></span>
<span data-ttu-id="b93f0-119">App 服務環境名稱</span><span class="sxs-lookup"><span data-stu-id="b93f0-119">App Service Environment Name</span></span>

```yaml
Type: String
Parameter Sets: WebAppParameterSet
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b93f0-120">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b93f0-120">-AseResourceGroupName</span></span>
<span data-ttu-id="b93f0-121">App 服務環境資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="b93f0-121">App Service Environment Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: WebAppParameterSet
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b93f0-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b93f0-122">-AsJob</span></span>
<span data-ttu-id="b93f0-123">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b93f0-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b93f0-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b93f0-124">-DefaultProfile</span></span>
<span data-ttu-id="b93f0-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b93f0-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b93f0-126">-GitRepositoryPath</span><span class="sxs-lookup"><span data-stu-id="b93f0-126">-GitRepositoryPath</span></span>
<span data-ttu-id="b93f0-127">GitHub 知識庫的路徑 containign 要部署的 web 應用程式。</span><span class="sxs-lookup"><span data-stu-id="b93f0-127">Path to the GitHub repository containign the web application to deploy.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b93f0-128">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="b93f0-128">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="b93f0-129">[忽略自訂主機名稱] 選項</span><span class="sxs-lookup"><span data-stu-id="b93f0-129">Ignore Custom Host Names Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WebAppParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b93f0-130">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="b93f0-130">-IgnoreSourceControl</span></span>
<span data-ttu-id="b93f0-131">[忽略來源控制] 選項</span><span class="sxs-lookup"><span data-stu-id="b93f0-131">Ignore Source Control Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WebAppParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b93f0-132">-IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="b93f0-132">-IncludeSourceWebAppSlots</span></span>
<span data-ttu-id="b93f0-133">[包括來源 WebApp 槽] 選項</span><span class="sxs-lookup"><span data-stu-id="b93f0-133">Include Source WebApp Slots Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WebAppParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b93f0-134">-位置</span><span class="sxs-lookup"><span data-stu-id="b93f0-134">-Location</span></span>
<span data-ttu-id="b93f0-135">位於</span><span class="sxs-lookup"><span data-stu-id="b93f0-135">Location</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: WebAppParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b93f0-136">-名稱</span><span class="sxs-lookup"><span data-stu-id="b93f0-136">-Name</span></span>
<span data-ttu-id="b93f0-137">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="b93f0-137">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: WebAppName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b93f0-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b93f0-138">-ResourceGroupName</span></span>
<span data-ttu-id="b93f0-139">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="b93f0-139">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: WebAppParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b93f0-140">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="b93f0-140">-SourceWebApp</span></span>
<span data-ttu-id="b93f0-141">來源 WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="b93f0-141">Source WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: WebAppParameterSet
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b93f0-142">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b93f0-142">-TrafficManagerProfile</span></span>
<span data-ttu-id="b93f0-143">現有流量管理器設定檔的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="b93f0-143">Resource Id of existing traffic manager profile</span></span>

```yaml
Type: String
Parameter Sets: WebAppParameterSet
Aliases: TrafficManagerProfileName, TrafficManagerProfileId

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b93f0-144">-確認</span><span class="sxs-lookup"><span data-stu-id="b93f0-144">-Confirm</span></span>
<span data-ttu-id="b93f0-145">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b93f0-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b93f0-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b93f0-146">-WhatIf</span></span>
<span data-ttu-id="b93f0-147">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b93f0-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b93f0-148">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b93f0-148">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b93f0-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b93f0-149">CommonParameters</span></span>
<span data-ttu-id="b93f0-150">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b93f0-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b93f0-151">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b93f0-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b93f0-152">輸入</span><span class="sxs-lookup"><span data-stu-id="b93f0-152">INPUTS</span></span>

### <span data-ttu-id="b93f0-153">網站地圖</span><span class="sxs-lookup"><span data-stu-id="b93f0-153">Site</span></span>
<span data-ttu-id="b93f0-154">形參 "SourceWebApp" 接受管線中 "Site" 類型的值</span><span class="sxs-lookup"><span data-stu-id="b93f0-154">Parameter 'SourceWebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="b93f0-155">輸出</span><span class="sxs-lookup"><span data-stu-id="b93f0-155">OUTPUTS</span></span>

### <span data-ttu-id="b93f0-156">[Microsoft Azure. 管理] 網站</span><span class="sxs-lookup"><span data-stu-id="b93f0-156">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="b93f0-157">筆記</span><span class="sxs-lookup"><span data-stu-id="b93f0-157">NOTES</span></span>

## <span data-ttu-id="b93f0-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="b93f0-158">RELATED LINKS</span></span>

[<span data-ttu-id="b93f0-159">AzWebApp</span><span class="sxs-lookup"><span data-stu-id="b93f0-159">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="b93f0-160">移除-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="b93f0-160">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="b93f0-161">重新開機-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="b93f0-161">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="b93f0-162">開始-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="b93f0-162">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="b93f0-163">停止 AzWebApp</span><span class="sxs-lookup"><span data-stu-id="b93f0-163">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


