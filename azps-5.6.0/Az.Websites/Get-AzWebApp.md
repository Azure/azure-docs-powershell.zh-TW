---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: A87ED954-9C09-4329-A005-ABFF36C45E6E
online version: https://docs.microsoft.com/powershell/module/az.websites/get-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebApp.md
ms.openlocfilehash: 32e71b33b3c440701e501c4b68d740dcf121001d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909893"
---
# <span data-ttu-id="1ec98-101">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="1ec98-101">Get-AzWebApp</span></span>

## <span data-ttu-id="1ec98-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1ec98-102">SYNOPSIS</span></span>
<span data-ttu-id="1ec98-103">在指定的資源群組中，獲得 Azure Web Apps。</span><span class="sxs-lookup"><span data-stu-id="1ec98-103">Gets Azure Web Apps in the specified resource group.</span></span>

## <span data-ttu-id="1ec98-104">語法</span><span class="sxs-lookup"><span data-stu-id="1ec98-104">SYNTAX</span></span>

### <span data-ttu-id="1ec98-105">S1</span><span class="sxs-lookup"><span data-stu-id="1ec98-105">S1</span></span>
```
Get-AzWebApp [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1ec98-106">S2</span><span class="sxs-lookup"><span data-stu-id="1ec98-106">S2</span></span>
```
Get-AzWebApp [-AppServicePlan] <PSAppServicePlan> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1ec98-107">S3</span><span class="sxs-lookup"><span data-stu-id="1ec98-107">S3</span></span>
```
Get-AzWebApp [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1ec98-108">描述</span><span class="sxs-lookup"><span data-stu-id="1ec98-108">DESCRIPTION</span></span>
<span data-ttu-id="1ec98-109">**Get-AzWebApp** Cmdlet 會取得 Azure Web App 相關資訊。</span><span class="sxs-lookup"><span data-stu-id="1ec98-109">The **Get-AzWebApp** cmdlet gets information about an Azure Web App.</span></span>

## <span data-ttu-id="1ec98-110">例子</span><span class="sxs-lookup"><span data-stu-id="1ec98-110">EXAMPLES</span></span>

### <span data-ttu-id="1ec98-111">範例 1：從資源群組取得 Web App</span><span class="sxs-lookup"><span data-stu-id="1ec98-111">Example 1: Get a Web App from a resource group</span></span>
```
PS C:\>Get-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="1ec98-112">此命令會獲得名稱為 ContosoSite 的 Web App，該 Web App 屬於資源群組 Default-Web-WestUS。</span><span class="sxs-lookup"><span data-stu-id="1ec98-112">This command gets the Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="1ec98-113">參數</span><span class="sxs-lookup"><span data-stu-id="1ec98-113">PARAMETERS</span></span>

### <span data-ttu-id="1ec98-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="1ec98-114">-AppServicePlan</span></span>
<span data-ttu-id="1ec98-115">應用程式服務計畫物件</span><span class="sxs-lookup"><span data-stu-id="1ec98-115">App Service Plan object</span></span>

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

### <span data-ttu-id="1ec98-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ec98-116">-DefaultProfile</span></span>
<span data-ttu-id="1ec98-117">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="1ec98-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1ec98-118">-位置</span><span class="sxs-lookup"><span data-stu-id="1ec98-118">-Location</span></span>
<span data-ttu-id="1ec98-119">位置</span><span class="sxs-lookup"><span data-stu-id="1ec98-119">Location</span></span>

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

### <span data-ttu-id="1ec98-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="1ec98-120">-Name</span></span>
<span data-ttu-id="1ec98-121">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="1ec98-121">WebApp Name</span></span>

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

### <span data-ttu-id="1ec98-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ec98-122">-ResourceGroupName</span></span>
<span data-ttu-id="1ec98-123">資源組名</span><span class="sxs-lookup"><span data-stu-id="1ec98-123">Resource Group Name</span></span>

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

### <span data-ttu-id="1ec98-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ec98-124">CommonParameters</span></span>
<span data-ttu-id="1ec98-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1ec98-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ec98-126">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="1ec98-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ec98-127">輸入</span><span class="sxs-lookup"><span data-stu-id="1ec98-127">INPUTS</span></span>

### <span data-ttu-id="1ec98-128">System.String</span><span class="sxs-lookup"><span data-stu-id="1ec98-128">System.String</span></span>

## <span data-ttu-id="1ec98-129">輸出</span><span class="sxs-lookup"><span data-stu-id="1ec98-129">OUTPUTS</span></span>

### <span data-ttu-id="1ec98-130">Microsoft.Azure.Commands.WebApps.models.PSSite</span><span class="sxs-lookup"><span data-stu-id="1ec98-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="1ec98-131">筆記</span><span class="sxs-lookup"><span data-stu-id="1ec98-131">NOTES</span></span>

## <span data-ttu-id="1ec98-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="1ec98-132">RELATED LINKS</span></span>

[<span data-ttu-id="1ec98-133">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="1ec98-133">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="1ec98-134">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="1ec98-134">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="1ec98-135">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="1ec98-135">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="1ec98-136">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="1ec98-136">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="1ec98-137">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="1ec98-137">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


