---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 32D45795-FBCD-4157-BF45-41BD1F61782E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/set-azurermappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmAppServicePlan.md
ms.openlocfilehash: 16b2c8df737047619366ebf6b75a4c2ed2264fdc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452935"
---
# <span data-ttu-id="0cabc-101">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="0cabc-101">Set-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="0cabc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0cabc-102">SYNOPSIS</span></span>
<span data-ttu-id="0cabc-103">設定 Azure App 服務方案。</span><span class="sxs-lookup"><span data-stu-id="0cabc-103">Sets an Azure App Service plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0cabc-104">句法</span><span class="sxs-lookup"><span data-stu-id="0cabc-104">SYNTAX</span></span>

### <span data-ttu-id="0cabc-105">S1</span><span class="sxs-lookup"><span data-stu-id="0cabc-105">S1</span></span>
```
Set-AzureRmAppServicePlan [[-AdminSiteName] <String>] [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [-PerSiteScaling <Boolean>] [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0cabc-106">S2</span><span class="sxs-lookup"><span data-stu-id="0cabc-106">S2</span></span>
```
Set-AzureRmAppServicePlan [-AppServicePlan] <ServerFarmWithRichSku> [-AsJob]
[-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0cabc-107">說明</span><span class="sxs-lookup"><span data-stu-id="0cabc-107">DESCRIPTION</span></span>
<span data-ttu-id="0cabc-108">**AzureRmAppServicePlan** Cmdlet 會設定 Azure App Service 方案。</span><span class="sxs-lookup"><span data-stu-id="0cabc-108">The **Set-AzureRmAppServicePlan** cmdlet sets an Azure App Service plan.</span></span>

## <span data-ttu-id="0cabc-109">示例</span><span class="sxs-lookup"><span data-stu-id="0cabc-109">EXAMPLES</span></span>

### <span data-ttu-id="0cabc-110">1：修改 App 服務方案</span><span class="sxs-lookup"><span data-stu-id="0cabc-110">1: Modify an App Service plan</span></span>
```
PS C:\>Set-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -PerSiteScaling $true
```

<span data-ttu-id="0cabc-111">這個命令會將 PerSiteScaling 選項設定為 true，該應用程式服務方案的名為 ContosoASP，且屬於名為 [預設-Web-WestUS] 的資源群組。</span><span class="sxs-lookup"><span data-stu-id="0cabc-111">This command sets the PerSiteScaling option to true on the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="0cabc-112">參數</span><span class="sxs-lookup"><span data-stu-id="0cabc-112">PARAMETERS</span></span>

### <span data-ttu-id="0cabc-113">-AdminSiteName</span><span class="sxs-lookup"><span data-stu-id="0cabc-113">-AdminSiteName</span></span>
<span data-ttu-id="0cabc-114">系統管理網站名稱</span><span class="sxs-lookup"><span data-stu-id="0cabc-114">Admin Site Name</span></span>

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

### <span data-ttu-id="0cabc-115">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="0cabc-115">-AppServicePlan</span></span>
<span data-ttu-id="0cabc-116">App Service 方案物件</span><span class="sxs-lookup"><span data-stu-id="0cabc-116">App Service Plan Object</span></span>

```yaml
Type: ServerFarmWithRichSku
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0cabc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cabc-117">-DefaultProfile</span></span>
<span data-ttu-id="0cabc-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0cabc-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0cabc-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="0cabc-119">-Name</span></span>
<span data-ttu-id="0cabc-120">App 服務方案名稱</span><span class="sxs-lookup"><span data-stu-id="0cabc-120">App Service Plan Name</span></span>

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

### <span data-ttu-id="0cabc-121">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="0cabc-121">-NumberofWorkers</span></span>
<span data-ttu-id="0cabc-122">員工人數</span><span class="sxs-lookup"><span data-stu-id="0cabc-122">Number Of Workers</span></span>

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

### <span data-ttu-id="0cabc-123">-PerSiteScaling</span><span class="sxs-lookup"><span data-stu-id="0cabc-123">-PerSiteScaling</span></span>
<span data-ttu-id="0cabc-124">每個網站縮放布林值</span><span class="sxs-lookup"><span data-stu-id="0cabc-124">Per Site Scaling Boolean</span></span>

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

### <span data-ttu-id="0cabc-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0cabc-125">-ResourceGroupName</span></span>
<span data-ttu-id="0cabc-126">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="0cabc-126">Resource Group Name</span></span>

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

### <span data-ttu-id="0cabc-127">層級</span><span class="sxs-lookup"><span data-stu-id="0cabc-127">-Tier</span></span>
<span data-ttu-id="0cabc-128">端</span><span class="sxs-lookup"><span data-stu-id="0cabc-128">Tier</span></span>

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

### <span data-ttu-id="0cabc-129">-WorkerSize</span><span class="sxs-lookup"><span data-stu-id="0cabc-129">-WorkerSize</span></span>
<span data-ttu-id="0cabc-130">工作人員大小</span><span class="sxs-lookup"><span data-stu-id="0cabc-130">Worker Size</span></span>

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
### <span data-ttu-id="0cabc-131">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0cabc-131">-AsJob</span></span>
<span data-ttu-id="0cabc-132">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="0cabc-132">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0cabc-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cabc-133">CommonParameters</span></span>
<span data-ttu-id="0cabc-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0cabc-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cabc-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0cabc-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cabc-136">輸入</span><span class="sxs-lookup"><span data-stu-id="0cabc-136">INPUTS</span></span>

### <span data-ttu-id="0cabc-137">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="0cabc-137">ServerFarmWithRichSku</span></span>
<span data-ttu-id="0cabc-138">形參 "AppServicePlan" 接受管線中 "ServerFarmWithRichSku" 類型的值</span><span class="sxs-lookup"><span data-stu-id="0cabc-138">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="0cabc-139">輸出</span><span class="sxs-lookup"><span data-stu-id="0cabc-139">OUTPUTS</span></span>

### <span data-ttu-id="0cabc-140">ServerFarmWithRichSku 中的 [網站]。</span><span class="sxs-lookup"><span data-stu-id="0cabc-140">Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku</span></span>

## <span data-ttu-id="0cabc-141">筆記</span><span class="sxs-lookup"><span data-stu-id="0cabc-141">NOTES</span></span>

## <span data-ttu-id="0cabc-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="0cabc-142">RELATED LINKS</span></span>

[<span data-ttu-id="0cabc-143">AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="0cabc-143">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="0cabc-144">新-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="0cabc-144">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="0cabc-145">移除-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="0cabc-145">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="0cabc-146">重新開機-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="0cabc-146">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="0cabc-147">開始-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="0cabc-147">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="0cabc-148">停止 AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="0cabc-148">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)

