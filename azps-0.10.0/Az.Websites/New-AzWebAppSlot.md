---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: D23BBF34-80C0-48B1-8E1C-6F345DEC61AD
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/new-Azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/New-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/New-AzWebAppSlot.md
ms.openlocfilehash: 41851c1492c3c14e3129ba04367580b09cf3ffb5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794962"
---
# <span data-ttu-id="5e5b6-101">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="5e5b6-101">New-AzWebAppSlot</span></span>

## <span data-ttu-id="5e5b6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5e5b6-102">SYNOPSIS</span></span>
<span data-ttu-id="5e5b6-103">建立 Azure Web App 槽。</span><span class="sxs-lookup"><span data-stu-id="5e5b6-103">Creates an Azure Web App slot.</span></span>

## <span data-ttu-id="5e5b6-104">句法</span><span class="sxs-lookup"><span data-stu-id="5e5b6-104">SYNTAX</span></span>

```
New-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [[-AppServicePlan] <String>] [[-SourceWebApp] <Site>] [-IgnoreSourceControl] [-IgnoreCustomHostNames]
 [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5e5b6-105">說明</span><span class="sxs-lookup"><span data-stu-id="5e5b6-105">DESCRIPTION</span></span>
<span data-ttu-id="5e5b6-106">**AzWebAppSlot** Cmdlet 會在指定的資源群組中使用指定的應用程式服務方案和資料中心來建立 Azure Web App 槽。</span><span class="sxs-lookup"><span data-stu-id="5e5b6-106">The **New-AzWebAppSlot** cmdlet creates an Azure Web App Slot in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="5e5b6-107">示例</span><span class="sxs-lookup"><span data-stu-id="5e5b6-107">EXAMPLES</span></span>

### <span data-ttu-id="5e5b6-108">範例1</span><span class="sxs-lookup"><span data-stu-id="5e5b6-108">Example 1</span></span>
```
PS C:\> New-AzWebAppSlot -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -AppServicePlan "ContosoServicePlan" -Slot "Slot001"
```

<span data-ttu-id="5e5b6-109">這個命令會在已有的 Web App 名稱 ContosoSite 中，建立一個名為 Slot001 的槽，在「資料中心」的現有資源群組中的 [預設-網路-WestUS] 西部我們。</span><span class="sxs-lookup"><span data-stu-id="5e5b6-109">This command creates a Slot named Slot001 under an existing Web App names ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="5e5b6-110">此命令使用名為 ContosoServicePlan 的現有應用程式服務方案。</span><span class="sxs-lookup"><span data-stu-id="5e5b6-110">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="5e5b6-111">參數</span><span class="sxs-lookup"><span data-stu-id="5e5b6-111">PARAMETERS</span></span>

### <span data-ttu-id="5e5b6-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="5e5b6-112">-AppServicePlan</span></span>
<span data-ttu-id="5e5b6-113">App 服務方案名稱</span><span class="sxs-lookup"><span data-stu-id="5e5b6-113">App Service Plan Name</span></span>

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

### <span data-ttu-id="5e5b6-114">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="5e5b6-114">-AppSettingsOverrides</span></span>
<span data-ttu-id="5e5b6-115">應用程式設定會覆寫 Hashtable</span><span class="sxs-lookup"><span data-stu-id="5e5b6-115">App Settings Overrides Hashtable</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e5b6-116">-AseName</span><span class="sxs-lookup"><span data-stu-id="5e5b6-116">-AseName</span></span>
<span data-ttu-id="5e5b6-117">App 服務環境名稱</span><span class="sxs-lookup"><span data-stu-id="5e5b6-117">App Service Environment Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e5b6-118">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e5b6-118">-AseResourceGroupName</span></span>
<span data-ttu-id="5e5b6-119">App 服務環境資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="5e5b6-119">App Service Environment Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e5b6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e5b6-120">-DefaultProfile</span></span>
<span data-ttu-id="5e5b6-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5e5b6-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5e5b6-122">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="5e5b6-122">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="5e5b6-123">[忽略自訂主機名稱] 選項</span><span class="sxs-lookup"><span data-stu-id="5e5b6-123">Ignore Custom HostNames Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e5b6-124">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="5e5b6-124">-IgnoreSourceControl</span></span>
<span data-ttu-id="5e5b6-125">[忽略來源控制] 選項</span><span class="sxs-lookup"><span data-stu-id="5e5b6-125">Ignore Source Control Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e5b6-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="5e5b6-126">-Name</span></span>
<span data-ttu-id="5e5b6-127">Webapp 名稱</span><span class="sxs-lookup"><span data-stu-id="5e5b6-127">Webapp Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e5b6-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e5b6-128">-ResourceGroupName</span></span>
<span data-ttu-id="5e5b6-129">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="5e5b6-129">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e5b6-130">-槽</span><span class="sxs-lookup"><span data-stu-id="5e5b6-130">-Slot</span></span>
<span data-ttu-id="5e5b6-131">Webapp 槽名稱</span><span class="sxs-lookup"><span data-stu-id="5e5b6-131">Webapp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e5b6-132">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="5e5b6-132">-SourceWebApp</span></span>
<span data-ttu-id="5e5b6-133">來源 WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="5e5b6-133">Source WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5e5b6-134">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5e5b6-134">-AsJob</span></span>
<span data-ttu-id="5e5b6-135">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5e5b6-135">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5e5b6-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e5b6-136">CommonParameters</span></span>
<span data-ttu-id="5e5b6-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5e5b6-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e5b6-138">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5e5b6-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e5b6-139">輸入</span><span class="sxs-lookup"><span data-stu-id="5e5b6-139">INPUTS</span></span>

### <span data-ttu-id="5e5b6-140">網站地圖</span><span class="sxs-lookup"><span data-stu-id="5e5b6-140">Site</span></span>
<span data-ttu-id="5e5b6-141">形參 "SourceWebApp" 接受管線中 "Site" 類型的值</span><span class="sxs-lookup"><span data-stu-id="5e5b6-141">Parameter 'SourceWebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="5e5b6-142">輸出</span><span class="sxs-lookup"><span data-stu-id="5e5b6-142">OUTPUTS</span></span>

## <span data-ttu-id="5e5b6-143">筆記</span><span class="sxs-lookup"><span data-stu-id="5e5b6-143">NOTES</span></span>

## <span data-ttu-id="5e5b6-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="5e5b6-144">RELATED LINKS</span></span>

[<span data-ttu-id="5e5b6-145">AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="5e5b6-145">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="5e5b6-146">移除-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="5e5b6-146">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="5e5b6-147">重新開機-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="5e5b6-147">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="5e5b6-148">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="5e5b6-148">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="5e5b6-149">開始-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="5e5b6-149">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="5e5b6-150">停止 AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="5e5b6-150">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="5e5b6-151">AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="5e5b6-151">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="5e5b6-152">AzWebApp</span><span class="sxs-lookup"><span data-stu-id="5e5b6-152">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
