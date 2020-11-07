---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: D23BBF34-80C0-48B1-8E1C-6F345DEC61AD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermwebappslot
schema: 2.0.0
ms.openlocfilehash: f41149c6abb946340acc06b847c72dcabcee18fe
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800618"
---
# <span data-ttu-id="faf15-101">New-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="faf15-101">New-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="faf15-102">摘要</span><span class="sxs-lookup"><span data-stu-id="faf15-102">SYNOPSIS</span></span>
<span data-ttu-id="faf15-103">建立 Azure Web App 槽。</span><span class="sxs-lookup"><span data-stu-id="faf15-103">Creates an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="faf15-104">句法</span><span class="sxs-lookup"><span data-stu-id="faf15-104">SYNTAX</span></span>

```
New-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [[-AppServicePlan] <String>] [[-SourceWebApp] <Site>] [-IgnoreSourceControl] [-IgnoreCustomHostNames]
 [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="faf15-105">說明</span><span class="sxs-lookup"><span data-stu-id="faf15-105">DESCRIPTION</span></span>
<span data-ttu-id="faf15-106">**AzureRmWebAppSlot** Cmdlet 會在指定的資源群組中使用指定的應用程式服務方案和資料中心來建立 Azure Web App 槽。</span><span class="sxs-lookup"><span data-stu-id="faf15-106">The **New-AzureRmWebAppSlot** cmdlet creates an Azure Web App Slot in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="faf15-107">示例</span><span class="sxs-lookup"><span data-stu-id="faf15-107">EXAMPLES</span></span>

### <span data-ttu-id="faf15-108">範例1</span><span class="sxs-lookup"><span data-stu-id="faf15-108">Example 1</span></span>
```
PS C:\> New-AzureRmWebAppSlot -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -AppServicePlan "ContosoServicePlan" -Slot "Slot001"
```

<span data-ttu-id="faf15-109">這個命令會在已有的 Web App 名稱 ContosoSite 中，建立一個名為 Slot001 的槽，在「資料中心」的現有資源群組中的 [預設-網路-WestUS] 西部我們。</span><span class="sxs-lookup"><span data-stu-id="faf15-109">This command creates a Slot named Slot001 under an existing Web App names ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="faf15-110">此命令使用名為 ContosoServicePlan 的現有應用程式服務方案。</span><span class="sxs-lookup"><span data-stu-id="faf15-110">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="faf15-111">參數</span><span class="sxs-lookup"><span data-stu-id="faf15-111">PARAMETERS</span></span>

### <span data-ttu-id="faf15-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="faf15-112">-AppServicePlan</span></span>
<span data-ttu-id="faf15-113">App 服務方案名稱</span><span class="sxs-lookup"><span data-stu-id="faf15-113">App Service Plan Name</span></span>

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

### <span data-ttu-id="faf15-114">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="faf15-114">-AppSettingsOverrides</span></span>
<span data-ttu-id="faf15-115">應用程式設定會覆寫 Hashtable</span><span class="sxs-lookup"><span data-stu-id="faf15-115">App Settings Overrides Hashtable</span></span>

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

### <span data-ttu-id="faf15-116">-AseName</span><span class="sxs-lookup"><span data-stu-id="faf15-116">-AseName</span></span>
<span data-ttu-id="faf15-117">App 服務環境名稱</span><span class="sxs-lookup"><span data-stu-id="faf15-117">App Service Environment Name</span></span>

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

### <span data-ttu-id="faf15-118">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="faf15-118">-AseResourceGroupName</span></span>
<span data-ttu-id="faf15-119">App 服務環境資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="faf15-119">App Service Environment Resource Group Name</span></span>

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

### <span data-ttu-id="faf15-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="faf15-120">-DefaultProfile</span></span>
<span data-ttu-id="faf15-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="faf15-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="faf15-122">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="faf15-122">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="faf15-123">[忽略自訂主機名稱] 選項</span><span class="sxs-lookup"><span data-stu-id="faf15-123">Ignore Custom HostNames Option</span></span>

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

### <span data-ttu-id="faf15-124">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="faf15-124">-IgnoreSourceControl</span></span>
<span data-ttu-id="faf15-125">[忽略來源控制] 選項</span><span class="sxs-lookup"><span data-stu-id="faf15-125">Ignore Source Control Option</span></span>

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

### <span data-ttu-id="faf15-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="faf15-126">-Name</span></span>
<span data-ttu-id="faf15-127">Webapp 名稱</span><span class="sxs-lookup"><span data-stu-id="faf15-127">Webapp Name</span></span>

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

### <span data-ttu-id="faf15-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="faf15-128">-ResourceGroupName</span></span>
<span data-ttu-id="faf15-129">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="faf15-129">Resource Group Name</span></span>

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

### <span data-ttu-id="faf15-130">-槽</span><span class="sxs-lookup"><span data-stu-id="faf15-130">-Slot</span></span>
<span data-ttu-id="faf15-131">Webapp 槽名稱</span><span class="sxs-lookup"><span data-stu-id="faf15-131">Webapp Slot Name</span></span>

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

### <span data-ttu-id="faf15-132">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="faf15-132">-SourceWebApp</span></span>
<span data-ttu-id="faf15-133">來源 WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="faf15-133">Source WebApp Object</span></span>

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

### <span data-ttu-id="faf15-134">-AsJob</span><span class="sxs-lookup"><span data-stu-id="faf15-134">-AsJob</span></span>
<span data-ttu-id="faf15-135">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="faf15-135">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="faf15-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="faf15-136">CommonParameters</span></span>
<span data-ttu-id="faf15-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="faf15-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="faf15-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="faf15-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="faf15-139">輸入</span><span class="sxs-lookup"><span data-stu-id="faf15-139">INPUTS</span></span>

### <span data-ttu-id="faf15-140">網站地圖</span><span class="sxs-lookup"><span data-stu-id="faf15-140">Site</span></span>
<span data-ttu-id="faf15-141">形參 "SourceWebApp" 接受管線中 "Site" 類型的值</span><span class="sxs-lookup"><span data-stu-id="faf15-141">Parameter 'SourceWebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="faf15-142">輸出</span><span class="sxs-lookup"><span data-stu-id="faf15-142">OUTPUTS</span></span>

## <span data-ttu-id="faf15-143">筆記</span><span class="sxs-lookup"><span data-stu-id="faf15-143">NOTES</span></span>

## <span data-ttu-id="faf15-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="faf15-144">RELATED LINKS</span></span>

[<span data-ttu-id="faf15-145">AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="faf15-145">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="faf15-146">移除-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="faf15-146">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="faf15-147">重新開機-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="faf15-147">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="faf15-148">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="faf15-148">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="faf15-149">開始-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="faf15-149">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="faf15-150">停止 AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="faf15-150">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="faf15-151">AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="faf15-151">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="faf15-152">AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="faf15-152">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
