---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 32D45795-FBCD-4157-BF45-41BD1F61782E
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/set-Azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Set-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Set-AzAppServicePlan.md
ms.openlocfilehash: b679b98e84f389e35e7dc291822049e554d40a9a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794943"
---
# <span data-ttu-id="e70df-101">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="e70df-101">Set-AzAppServicePlan</span></span>

## <span data-ttu-id="e70df-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e70df-102">SYNOPSIS</span></span>
<span data-ttu-id="e70df-103">設定 Azure App 服務方案。</span><span class="sxs-lookup"><span data-stu-id="e70df-103">Sets an Azure App Service plan.</span></span>

## <span data-ttu-id="e70df-104">句法</span><span class="sxs-lookup"><span data-stu-id="e70df-104">SYNTAX</span></span>

### <span data-ttu-id="e70df-105">S1</span><span class="sxs-lookup"><span data-stu-id="e70df-105">S1</span></span>
```
Set-AzAppServicePlan [[-AdminSiteName] <String>] [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [-PerSiteScaling <Boolean>] [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e70df-106">S2</span><span class="sxs-lookup"><span data-stu-id="e70df-106">S2</span></span>
```
Set-AzAppServicePlan [-AppServicePlan] <AppServicePlan> [-AsJob]
[-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e70df-107">說明</span><span class="sxs-lookup"><span data-stu-id="e70df-107">DESCRIPTION</span></span>
<span data-ttu-id="e70df-108">**AzAppServicePlan** Cmdlet 會設定 Azure App Service 方案。</span><span class="sxs-lookup"><span data-stu-id="e70df-108">The **Set-AzAppServicePlan** cmdlet sets an Azure App Service plan.</span></span>

## <span data-ttu-id="e70df-109">示例</span><span class="sxs-lookup"><span data-stu-id="e70df-109">EXAMPLES</span></span>

### <span data-ttu-id="e70df-110">1：修改 App 服務方案</span><span class="sxs-lookup"><span data-stu-id="e70df-110">1: Modify an App Service plan</span></span>
```
PS C:\>Set-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -PerSiteScaling $true
```

<span data-ttu-id="e70df-111">這個命令會將 PerSiteScaling 選項設定為 true，該應用程式服務方案的名為 ContosoASP，且屬於名為 [預設-Web-WestUS] 的資源群組。</span><span class="sxs-lookup"><span data-stu-id="e70df-111">This command sets the PerSiteScaling option to true on the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="e70df-112">參數</span><span class="sxs-lookup"><span data-stu-id="e70df-112">PARAMETERS</span></span>

### <span data-ttu-id="e70df-113">-AdminSiteName</span><span class="sxs-lookup"><span data-stu-id="e70df-113">-AdminSiteName</span></span>
<span data-ttu-id="e70df-114">系統管理網站名稱</span><span class="sxs-lookup"><span data-stu-id="e70df-114">Admin Site Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e70df-115">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="e70df-115">-AppServicePlan</span></span>
<span data-ttu-id="e70df-116">App Service 方案物件</span><span class="sxs-lookup"><span data-stu-id="e70df-116">App Service Plan Object</span></span>

```yaml
Type: AppServicePlan
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e70df-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e70df-117">-DefaultProfile</span></span>
<span data-ttu-id="e70df-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e70df-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e70df-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="e70df-119">-Name</span></span>
<span data-ttu-id="e70df-120">App 服務方案名稱</span><span class="sxs-lookup"><span data-stu-id="e70df-120">App Service Plan Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e70df-121">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="e70df-121">-NumberofWorkers</span></span>
<span data-ttu-id="e70df-122">員工人數</span><span class="sxs-lookup"><span data-stu-id="e70df-122">Number Of Workers</span></span>

```yaml
Type: Int32
Parameter Sets: S1
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e70df-123">-PerSiteScaling</span><span class="sxs-lookup"><span data-stu-id="e70df-123">-PerSiteScaling</span></span>
<span data-ttu-id="e70df-124">每個網站縮放布林值</span><span class="sxs-lookup"><span data-stu-id="e70df-124">Per Site Scaling Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e70df-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e70df-125">-ResourceGroupName</span></span>
<span data-ttu-id="e70df-126">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="e70df-126">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e70df-127">層級</span><span class="sxs-lookup"><span data-stu-id="e70df-127">-Tier</span></span>
<span data-ttu-id="e70df-128">端</span><span class="sxs-lookup"><span data-stu-id="e70df-128">Tier</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 
Accepted values: Free, Shared, Basic, Standard, Premium, PremiumV2

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e70df-129">-WorkerSize</span><span class="sxs-lookup"><span data-stu-id="e70df-129">-WorkerSize</span></span>
<span data-ttu-id="e70df-130">工作人員大小</span><span class="sxs-lookup"><span data-stu-id="e70df-130">Worker Size</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 
Accepted values: Small, Medium, Large, ExtraLarge

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="e70df-131">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e70df-131">-AsJob</span></span>
<span data-ttu-id="e70df-132">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e70df-132">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e70df-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e70df-133">CommonParameters</span></span>
<span data-ttu-id="e70df-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e70df-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e70df-135">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e70df-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e70df-136">輸入</span><span class="sxs-lookup"><span data-stu-id="e70df-136">INPUTS</span></span>

### <span data-ttu-id="e70df-137">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="e70df-137">ServerFarmWithRichSku</span></span>
<span data-ttu-id="e70df-138">形參 "AppServicePlan" 接受管線中 "ServerFarmWithRichSku" 類型的值</span><span class="sxs-lookup"><span data-stu-id="e70df-138">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="e70df-139">輸出</span><span class="sxs-lookup"><span data-stu-id="e70df-139">OUTPUTS</span></span>

### <span data-ttu-id="e70df-140">ServerFarmWithRichSku 中的 [網站]。</span><span class="sxs-lookup"><span data-stu-id="e70df-140">Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku</span></span>

## <span data-ttu-id="e70df-141">筆記</span><span class="sxs-lookup"><span data-stu-id="e70df-141">NOTES</span></span>

## <span data-ttu-id="e70df-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="e70df-142">RELATED LINKS</span></span>

[<span data-ttu-id="e70df-143">AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e70df-143">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="e70df-144">新-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e70df-144">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="e70df-145">移除-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e70df-145">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="e70df-146">重新開機-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e70df-146">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="e70df-147">開始-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e70df-147">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="e70df-148">停止 AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e70df-148">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


