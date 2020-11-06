---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 32D45795-FBCD-4157-BF45-41BD1F61782E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmAppServicePlan.md
ms.openlocfilehash: 4b6270a6d56b8f210b2f03311bf19bb09950f361
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447107"
---
# <span data-ttu-id="3c24f-101">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="3c24f-101">Set-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="3c24f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3c24f-102">SYNOPSIS</span></span>
<span data-ttu-id="3c24f-103">設定 Azure App 服務方案。</span><span class="sxs-lookup"><span data-stu-id="3c24f-103">Sets an Azure App Service plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3c24f-104">句法</span><span class="sxs-lookup"><span data-stu-id="3c24f-104">SYNTAX</span></span>

### <span data-ttu-id="3c24f-105">S1</span><span class="sxs-lookup"><span data-stu-id="3c24f-105">S1</span></span>
```
Set-AzureRmAppServicePlan [[-AdminSiteName] <String>] [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [-PerSiteScaling <Boolean>] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c24f-106">S2</span><span class="sxs-lookup"><span data-stu-id="3c24f-106">S2</span></span>
```
Set-AzureRmAppServicePlan [-AppServicePlan] <ServerFarmWithRichSku> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3c24f-107">說明</span><span class="sxs-lookup"><span data-stu-id="3c24f-107">DESCRIPTION</span></span>
<span data-ttu-id="3c24f-108">**AzureRmAppServicePlan** Cmdlet 會設定 Azure App Service 方案。</span><span class="sxs-lookup"><span data-stu-id="3c24f-108">The **Set-AzureRmAppServicePlan** cmdlet sets an Azure App Service plan.</span></span>

## <span data-ttu-id="3c24f-109">示例</span><span class="sxs-lookup"><span data-stu-id="3c24f-109">EXAMPLES</span></span>

### <span data-ttu-id="3c24f-110">1：修改 App 服務方案</span><span class="sxs-lookup"><span data-stu-id="3c24f-110">1: Modify an App Service plan</span></span>
```
PS C:\>Set-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -PerSiteScaling $true
```

<span data-ttu-id="3c24f-111">這個命令會將 PerSiteScaling 選項設定為 true，該應用程式服務方案的名為 ContosoASP，且屬於名為 [預設-Web-WestUS] 的資源群組。</span><span class="sxs-lookup"><span data-stu-id="3c24f-111">This command sets the PerSiteScaling option to true on the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="3c24f-112">參數</span><span class="sxs-lookup"><span data-stu-id="3c24f-112">PARAMETERS</span></span>

### <span data-ttu-id="3c24f-113">-AdminSiteName</span><span class="sxs-lookup"><span data-stu-id="3c24f-113">-AdminSiteName</span></span>
<span data-ttu-id="3c24f-114">系統管理網站名稱</span><span class="sxs-lookup"><span data-stu-id="3c24f-114">Admin Site Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c24f-115">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="3c24f-115">-AppServicePlan</span></span>
<span data-ttu-id="3c24f-116">App Service 方案物件</span><span class="sxs-lookup"><span data-stu-id="3c24f-116">App Service Plan Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3c24f-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="3c24f-117">-Name</span></span>
<span data-ttu-id="3c24f-118">App 服務方案名稱</span><span class="sxs-lookup"><span data-stu-id="3c24f-118">App Service Plan Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c24f-119">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="3c24f-119">-NumberofWorkers</span></span>
<span data-ttu-id="3c24f-120">員工人數</span><span class="sxs-lookup"><span data-stu-id="3c24f-120">Number Of Workers</span></span>

```yaml
Type: System.Int32
Parameter Sets: S1
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c24f-121">-PerSiteScaling</span><span class="sxs-lookup"><span data-stu-id="3c24f-121">-PerSiteScaling</span></span>
<span data-ttu-id="3c24f-122">每個網站縮放布林值</span><span class="sxs-lookup"><span data-stu-id="3c24f-122">Per Site Scaling Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c24f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c24f-123">-ResourceGroupName</span></span>
<span data-ttu-id="3c24f-124">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="3c24f-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c24f-125">層級</span><span class="sxs-lookup"><span data-stu-id="3c24f-125">-Tier</span></span>
<span data-ttu-id="3c24f-126">端</span><span class="sxs-lookup"><span data-stu-id="3c24f-126">Tier</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 
Accepted values: Free, Shared, Basic, Standard, Premium

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c24f-127">-WorkerSize</span><span class="sxs-lookup"><span data-stu-id="3c24f-127">-WorkerSize</span></span>
<span data-ttu-id="3c24f-128">工作人員大小</span><span class="sxs-lookup"><span data-stu-id="3c24f-128">Worker Size</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 
Accepted values: Small, Medium, Large, ExtraLarge

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c24f-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c24f-129">-DefaultProfile</span></span>
<span data-ttu-id="3c24f-130">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3c24f-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3c24f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c24f-131">CommonParameters</span></span>
<span data-ttu-id="3c24f-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3c24f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c24f-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3c24f-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c24f-134">輸入</span><span class="sxs-lookup"><span data-stu-id="3c24f-134">INPUTS</span></span>

### <span data-ttu-id="3c24f-135">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="3c24f-135">ServerFarmWithRichSku</span></span>
<span data-ttu-id="3c24f-136">形參 "AppServicePlan" 接受管線中 "ServerFarmWithRichSku" 類型的值</span><span class="sxs-lookup"><span data-stu-id="3c24f-136">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="3c24f-137">輸出</span><span class="sxs-lookup"><span data-stu-id="3c24f-137">OUTPUTS</span></span>

### <span data-ttu-id="3c24f-138">ServerFarmWithRichSku 中的 [網站]。</span><span class="sxs-lookup"><span data-stu-id="3c24f-138">Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku</span></span>

## <span data-ttu-id="3c24f-139">筆記</span><span class="sxs-lookup"><span data-stu-id="3c24f-139">NOTES</span></span>

## <span data-ttu-id="3c24f-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="3c24f-140">RELATED LINKS</span></span>

[<span data-ttu-id="3c24f-141">AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="3c24f-141">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="3c24f-142">新-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="3c24f-142">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="3c24f-143">移除-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="3c24f-143">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="3c24f-144">重新開機-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="3c24f-144">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="3c24f-145">開始-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="3c24f-145">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="3c24f-146">停止 AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="3c24f-146">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


