---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: A87ED954-9C09-4329-A005-ABFF36C45E6E
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebApp.md
ms.openlocfilehash: 7dc1d2c5d6be1fd920ec9fb4eb90bf73b2c464b9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957164"
---
# <span data-ttu-id="49cdc-101">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="49cdc-101">Get-AzWebApp</span></span>

## <span data-ttu-id="49cdc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="49cdc-102">SYNOPSIS</span></span>
<span data-ttu-id="49cdc-103">在指定的資源群組中取得 Azure Web Apps。</span><span class="sxs-lookup"><span data-stu-id="49cdc-103">Gets Azure Web Apps in the specified resource group.</span></span>

## <span data-ttu-id="49cdc-104">句法</span><span class="sxs-lookup"><span data-stu-id="49cdc-104">SYNTAX</span></span>

### <span data-ttu-id="49cdc-105">S1</span><span class="sxs-lookup"><span data-stu-id="49cdc-105">S1</span></span>
```
Get-AzWebApp [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="49cdc-106">S2</span><span class="sxs-lookup"><span data-stu-id="49cdc-106">S2</span></span>
```
Get-AzWebApp [-AppServicePlan] <PSAppServicePlan> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="49cdc-107">S3</span><span class="sxs-lookup"><span data-stu-id="49cdc-107">S3</span></span>
```
Get-AzWebApp [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="49cdc-108">說明</span><span class="sxs-lookup"><span data-stu-id="49cdc-108">DESCRIPTION</span></span>
<span data-ttu-id="49cdc-109">**AzWebApp** Cmdlet 會取得 Azure Web App 的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="49cdc-109">The **Get-AzWebApp** cmdlet gets information about an Azure Web App.</span></span>

## <span data-ttu-id="49cdc-110">示例</span><span class="sxs-lookup"><span data-stu-id="49cdc-110">EXAMPLES</span></span>

### <span data-ttu-id="49cdc-111">範例1：從資源群組取得 Web 應用程式</span><span class="sxs-lookup"><span data-stu-id="49cdc-111">Example 1: Get a Web App from a resource group</span></span>
```
PS C:\>Get-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="49cdc-112">這個命令會取得屬於資源群組 Default-Web WestUS 的名為 ContosoSite 的 Web App。</span><span class="sxs-lookup"><span data-stu-id="49cdc-112">This command gets the Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="49cdc-113">參數</span><span class="sxs-lookup"><span data-stu-id="49cdc-113">PARAMETERS</span></span>

### <span data-ttu-id="49cdc-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="49cdc-114">-AppServicePlan</span></span>
<span data-ttu-id="49cdc-115">App Service 方案物件</span><span class="sxs-lookup"><span data-stu-id="49cdc-115">App Service Plan object</span></span>

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

### <span data-ttu-id="49cdc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49cdc-116">-DefaultProfile</span></span>
<span data-ttu-id="49cdc-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="49cdc-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49cdc-118">-位置</span><span class="sxs-lookup"><span data-stu-id="49cdc-118">-Location</span></span>
<span data-ttu-id="49cdc-119">位於</span><span class="sxs-lookup"><span data-stu-id="49cdc-119">Location</span></span>

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

### <span data-ttu-id="49cdc-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="49cdc-120">-Name</span></span>
<span data-ttu-id="49cdc-121">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="49cdc-121">WebApp Name</span></span>

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

### <span data-ttu-id="49cdc-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49cdc-122">-ResourceGroupName</span></span>
<span data-ttu-id="49cdc-123">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="49cdc-123">Resource Group Name</span></span>

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

### <span data-ttu-id="49cdc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49cdc-124">CommonParameters</span></span>
<span data-ttu-id="49cdc-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="49cdc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49cdc-126">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="49cdc-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49cdc-127">輸入</span><span class="sxs-lookup"><span data-stu-id="49cdc-127">INPUTS</span></span>

### <span data-ttu-id="49cdc-128">System.object</span><span class="sxs-lookup"><span data-stu-id="49cdc-128">System.String</span></span>

## <span data-ttu-id="49cdc-129">輸出</span><span class="sxs-lookup"><span data-stu-id="49cdc-129">OUTPUTS</span></span>

### <span data-ttu-id="49cdc-130">PSSite 中的 WebApps。</span><span class="sxs-lookup"><span data-stu-id="49cdc-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="49cdc-131">筆記</span><span class="sxs-lookup"><span data-stu-id="49cdc-131">NOTES</span></span>

## <span data-ttu-id="49cdc-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="49cdc-132">RELATED LINKS</span></span>

[<span data-ttu-id="49cdc-133">新-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="49cdc-133">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="49cdc-134">移除-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="49cdc-134">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="49cdc-135">重新開機-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="49cdc-135">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="49cdc-136">開始-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="49cdc-136">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="49cdc-137">停止 AzWebApp</span><span class="sxs-lookup"><span data-stu-id="49cdc-137">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


