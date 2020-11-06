---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: A87ED954-9C09-4329-A005-ABFF36C45E6E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebApp.md
ms.openlocfilehash: 83afdb179a9c0f135fd17827ff59f89ad117e3b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449670"
---
# <span data-ttu-id="c1e14-101">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="c1e14-101">Get-AzureRmWebApp</span></span>

## <span data-ttu-id="c1e14-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c1e14-102">SYNOPSIS</span></span>
<span data-ttu-id="c1e14-103">在指定的資源群組中取得 Azure Web Apps。</span><span class="sxs-lookup"><span data-stu-id="c1e14-103">Gets Azure Web Apps in the specified resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c1e14-104">句法</span><span class="sxs-lookup"><span data-stu-id="c1e14-104">SYNTAX</span></span>

### <span data-ttu-id="c1e14-105">S1</span><span class="sxs-lookup"><span data-stu-id="c1e14-105">S1</span></span>
```
Get-AzureRmWebApp [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c1e14-106">S2</span><span class="sxs-lookup"><span data-stu-id="c1e14-106">S2</span></span>
```
Get-AzureRmWebApp [-AppServicePlan] <PSAppServicePlan> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c1e14-107">S3</span><span class="sxs-lookup"><span data-stu-id="c1e14-107">S3</span></span>
```
Get-AzureRmWebApp [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c1e14-108">說明</span><span class="sxs-lookup"><span data-stu-id="c1e14-108">DESCRIPTION</span></span>
<span data-ttu-id="c1e14-109">**AzureRmWebApp** Cmdlet 會取得 Azure Web App 的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="c1e14-109">The **Get-AzureRmWebApp** cmdlet gets information about an Azure Web App.</span></span>

## <span data-ttu-id="c1e14-110">示例</span><span class="sxs-lookup"><span data-stu-id="c1e14-110">EXAMPLES</span></span>

### <span data-ttu-id="c1e14-111">範例1：從資源群組取得 Web 應用程式</span><span class="sxs-lookup"><span data-stu-id="c1e14-111">Example 1: Get a Web App from a resource group</span></span>
```
PS C:\>Get-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="c1e14-112">這個命令會取得屬於資源群組 Default-Web WestUS 的名為 ContosoSite 的 Web App。</span><span class="sxs-lookup"><span data-stu-id="c1e14-112">This command gets the Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="c1e14-113">參數</span><span class="sxs-lookup"><span data-stu-id="c1e14-113">PARAMETERS</span></span>

### <span data-ttu-id="c1e14-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="c1e14-114">-AppServicePlan</span></span>
<span data-ttu-id="c1e14-115">App Service 方案物件</span><span class="sxs-lookup"><span data-stu-id="c1e14-115">App Service Plan object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1e14-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1e14-116">-DefaultProfile</span></span>
<span data-ttu-id="c1e14-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c1e14-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c1e14-118">-位置</span><span class="sxs-lookup"><span data-stu-id="c1e14-118">-Location</span></span>
<span data-ttu-id="c1e14-119">位於</span><span class="sxs-lookup"><span data-stu-id="c1e14-119">Location</span></span>

```yaml
Type: System.String
Parameter Sets: S3
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1e14-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="c1e14-120">-Name</span></span>
<span data-ttu-id="c1e14-121">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="c1e14-121">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1e14-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1e14-122">-ResourceGroupName</span></span>
<span data-ttu-id="c1e14-123">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="c1e14-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1e14-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1e14-124">CommonParameters</span></span>
<span data-ttu-id="c1e14-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c1e14-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1e14-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c1e14-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1e14-127">輸入</span><span class="sxs-lookup"><span data-stu-id="c1e14-127">INPUTS</span></span>

### <span data-ttu-id="c1e14-128">System.object</span><span class="sxs-lookup"><span data-stu-id="c1e14-128">System.String</span></span>

## <span data-ttu-id="c1e14-129">輸出</span><span class="sxs-lookup"><span data-stu-id="c1e14-129">OUTPUTS</span></span>

### <span data-ttu-id="c1e14-130">[Microsoft Azure. 管理] 網站</span><span class="sxs-lookup"><span data-stu-id="c1e14-130">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="c1e14-131">筆記</span><span class="sxs-lookup"><span data-stu-id="c1e14-131">NOTES</span></span>

## <span data-ttu-id="c1e14-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="c1e14-132">RELATED LINKS</span></span>

[<span data-ttu-id="c1e14-133">新-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="c1e14-133">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="c1e14-134">移除-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="c1e14-134">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="c1e14-135">重新開機-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="c1e14-135">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="c1e14-136">開始-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="c1e14-136">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="c1e14-137">停止 AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="c1e14-137">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


