---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: D6D4E733-31AE-4ABE-8C78-583EC48C56B8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebApp.md
ms.openlocfilehash: 4948de891815345efdc0b3f4ec39fb1874e510b8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456336"
---
# <span data-ttu-id="47352-101">New-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="47352-101">New-AzureRmWebApp</span></span>

## <span data-ttu-id="47352-102">摘要</span><span class="sxs-lookup"><span data-stu-id="47352-102">SYNOPSIS</span></span>
<span data-ttu-id="47352-103">建立 Azure Web App。</span><span class="sxs-lookup"><span data-stu-id="47352-103">Creates an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="47352-104">句法</span><span class="sxs-lookup"><span data-stu-id="47352-104">SYNTAX</span></span>

### <span data-ttu-id="47352-105">S1 (預設) </span><span class="sxs-lookup"><span data-stu-id="47352-105">S1 (Default)</span></span>
```
New-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-AppServicePlan] <String>] [[-SourceWebApp] <Site>] [[-TrafficManagerProfileId] <String>]
 [-IgnoreSourceControl] [-IgnoreCustomHostNames] [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>]
 [[-AseResourceGroupName] <String>] [-IncludeSourceWebAppSlots] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="47352-106">S2</span><span class="sxs-lookup"><span data-stu-id="47352-106">S2</span></span>
```
New-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-AppServicePlan] <String>] [[-SourceWebApp] <Site>] [[-TrafficManagerProfileName] <String>]
 [-IgnoreSourceControl] [-IgnoreCustomHostNames] [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>]
 [[-AseResourceGroupName] <String>] [-IncludeSourceWebAppSlots] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="47352-107">說明</span><span class="sxs-lookup"><span data-stu-id="47352-107">DESCRIPTION</span></span>
<span data-ttu-id="47352-108">**AzureRmWebApp** Cmdlet 會在指定的資源群組中，使用指定的應用程式服務方案和資料中心來建立 Azure Web App。</span><span class="sxs-lookup"><span data-stu-id="47352-108">The **New-AzureRmWebApp** cmdlet creates an Azure Web App in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="47352-109">示例</span><span class="sxs-lookup"><span data-stu-id="47352-109">EXAMPLES</span></span>

### <span data-ttu-id="47352-110">範例1：建立 Web 應用程式</span><span class="sxs-lookup"><span data-stu-id="47352-110">Example 1: Create a Web App</span></span>
```
PS C:\>New-AzureRmWebApp -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -Location "West US" -AppServicePlan "ContosoServicePlan"
```

<span data-ttu-id="47352-111">這個命令會在資料中心的名為「預設-Web-WestUS」的現有資源群組中，建立名為 ContosoSite 的 Azure Web App。</span><span class="sxs-lookup"><span data-stu-id="47352-111">This command creates an Azure Web App named ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="47352-112">此命令使用名為 ContosoServicePlan 的現有應用程式服務方案。</span><span class="sxs-lookup"><span data-stu-id="47352-112">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="47352-113">參數</span><span class="sxs-lookup"><span data-stu-id="47352-113">PARAMETERS</span></span>

### <span data-ttu-id="47352-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="47352-114">-AppServicePlan</span></span>
<span data-ttu-id="47352-115">App 服務方案名稱</span><span class="sxs-lookup"><span data-stu-id="47352-115">App Service Plan Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47352-116">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="47352-116">-AppSettingsOverrides</span></span>
<span data-ttu-id="47352-117">應用程式設定會覆寫 HashTable</span><span class="sxs-lookup"><span data-stu-id="47352-117">App Settings Overrides HashTable</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47352-118">-AseName</span><span class="sxs-lookup"><span data-stu-id="47352-118">-AseName</span></span>
<span data-ttu-id="47352-119">App 服務環境名稱</span><span class="sxs-lookup"><span data-stu-id="47352-119">App Service Environment Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47352-120">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47352-120">-AseResourceGroupName</span></span>
<span data-ttu-id="47352-121">App 服務環境資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="47352-121">App Service Environment Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47352-122">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="47352-122">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="47352-123">[忽略自訂主機名稱] 選項</span><span class="sxs-lookup"><span data-stu-id="47352-123">Ignore Custom Host Names Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47352-124">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="47352-124">-IgnoreSourceControl</span></span>
<span data-ttu-id="47352-125">[忽略來源控制] 選項</span><span class="sxs-lookup"><span data-stu-id="47352-125">Ignore Source Control Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47352-126">-IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="47352-126">-IncludeSourceWebAppSlots</span></span>
<span data-ttu-id="47352-127">[包括來源 WebApp 槽] 選項</span><span class="sxs-lookup"><span data-stu-id="47352-127">Include Source WebApp Slots Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47352-128">-位置</span><span class="sxs-lookup"><span data-stu-id="47352-128">-Location</span></span>
<span data-ttu-id="47352-129">位於</span><span class="sxs-lookup"><span data-stu-id="47352-129">Location</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47352-130">-名稱</span><span class="sxs-lookup"><span data-stu-id="47352-130">-Name</span></span>
<span data-ttu-id="47352-131">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="47352-131">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47352-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47352-132">-ResourceGroupName</span></span>
<span data-ttu-id="47352-133">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="47352-133">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47352-134">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="47352-134">-SourceWebApp</span></span>
<span data-ttu-id="47352-135">來源 WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="47352-135">Source WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="47352-136">-TrafficManagerProfileId</span><span class="sxs-lookup"><span data-stu-id="47352-136">-TrafficManagerProfileId</span></span>
<span data-ttu-id="47352-137">流量管理器設定檔識別碼</span><span class="sxs-lookup"><span data-stu-id="47352-137">Traffic Manager Profile Id</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47352-138">-TrafficManagerProfileName</span><span class="sxs-lookup"><span data-stu-id="47352-138">-TrafficManagerProfileName</span></span>
<span data-ttu-id="47352-139">流量管理器設定檔名稱</span><span class="sxs-lookup"><span data-stu-id="47352-139">Traffic Manager Profile Name</span></span>

```yaml
Type: System.String
Parameter Sets: S2
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47352-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47352-140">-DefaultProfile</span></span>
<span data-ttu-id="47352-141">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="47352-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47352-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47352-142">CommonParameters</span></span>
<span data-ttu-id="47352-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="47352-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47352-144">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="47352-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47352-145">輸入</span><span class="sxs-lookup"><span data-stu-id="47352-145">INPUTS</span></span>

### <span data-ttu-id="47352-146">網站地圖</span><span class="sxs-lookup"><span data-stu-id="47352-146">Site</span></span>
<span data-ttu-id="47352-147">形參 "SourceWebApp" 接受管線中 "Site" 類型的值</span><span class="sxs-lookup"><span data-stu-id="47352-147">Parameter 'SourceWebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="47352-148">輸出</span><span class="sxs-lookup"><span data-stu-id="47352-148">OUTPUTS</span></span>

## <span data-ttu-id="47352-149">筆記</span><span class="sxs-lookup"><span data-stu-id="47352-149">NOTES</span></span>

## <span data-ttu-id="47352-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="47352-150">RELATED LINKS</span></span>

[<span data-ttu-id="47352-151">AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="47352-151">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="47352-152">移除-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="47352-152">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="47352-153">重新開機-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="47352-153">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="47352-154">開始-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="47352-154">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="47352-155">停止 AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="47352-155">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


