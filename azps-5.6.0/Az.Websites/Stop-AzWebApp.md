---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: A12FFDB1-9849-4150-9716-068BE6EFC681
online version: https://docs.microsoft.com/powershell/module/az.websites/stop-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Stop-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Stop-AzWebApp.md
ms.openlocfilehash: 102dbd678fe6fe46034a43c46cb713428b8564d5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916806"
---
# <span data-ttu-id="a7059-101">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a7059-101">Stop-AzWebApp</span></span>

## <span data-ttu-id="a7059-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a7059-102">SYNOPSIS</span></span>
<span data-ttu-id="a7059-103">停止 Azure Web App。</span><span class="sxs-lookup"><span data-stu-id="a7059-103">Stops an Azure Web App.</span></span>

## <span data-ttu-id="a7059-104">語法</span><span class="sxs-lookup"><span data-stu-id="a7059-104">SYNTAX</span></span>

### <span data-ttu-id="a7059-105">S1</span><span class="sxs-lookup"><span data-stu-id="a7059-105">S1</span></span>
```
Stop-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a7059-106">S2</span><span class="sxs-lookup"><span data-stu-id="a7059-106">S2</span></span>
```
Stop-AzWebApp [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a7059-107">描述</span><span class="sxs-lookup"><span data-stu-id="a7059-107">DESCRIPTION</span></span>
<span data-ttu-id="a7059-108">**Stop-AzWebApp** Cmdlet 會停止 Azure Web App。</span><span class="sxs-lookup"><span data-stu-id="a7059-108">The **Stop-AzWebApp** cmdlet stops an Azure Web App.</span></span>

## <span data-ttu-id="a7059-109">例子</span><span class="sxs-lookup"><span data-stu-id="a7059-109">EXAMPLES</span></span>

### <span data-ttu-id="a7059-110">範例 1：停止 Web App</span><span class="sxs-lookup"><span data-stu-id="a7059-110">Example 1: Stop a Web App</span></span>
```
PS C:\>Stop-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="a7059-111">此命令會停止名為 ContosoWebApp 的 Web App，該 Web App 屬於 Default-Web-WestUS 資源群組。</span><span class="sxs-lookup"><span data-stu-id="a7059-111">This command stops the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="a7059-112">參數</span><span class="sxs-lookup"><span data-stu-id="a7059-112">PARAMETERS</span></span>

### <span data-ttu-id="a7059-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7059-113">-DefaultProfile</span></span>
<span data-ttu-id="a7059-114">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a7059-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7059-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="a7059-115">-Name</span></span>
<span data-ttu-id="a7059-116">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="a7059-116">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7059-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7059-117">-ResourceGroupName</span></span>
<span data-ttu-id="a7059-118">資源組名</span><span class="sxs-lookup"><span data-stu-id="a7059-118">Resource Group Name</span></span>

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

### <span data-ttu-id="a7059-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="a7059-119">-WebApp</span></span>
<span data-ttu-id="a7059-120">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="a7059-120">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a7059-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7059-121">CommonParameters</span></span>
<span data-ttu-id="a7059-122">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a7059-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7059-123">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="a7059-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7059-124">輸入</span><span class="sxs-lookup"><span data-stu-id="a7059-124">INPUTS</span></span>

### <span data-ttu-id="a7059-125">System.String</span><span class="sxs-lookup"><span data-stu-id="a7059-125">System.String</span></span>

### <span data-ttu-id="a7059-126">Microsoft.Azure.Commands.WebApps.models.PSSite</span><span class="sxs-lookup"><span data-stu-id="a7059-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="a7059-127">輸出</span><span class="sxs-lookup"><span data-stu-id="a7059-127">OUTPUTS</span></span>

### <span data-ttu-id="a7059-128">Microsoft.Azure.Commands.WebApps.models.PSSite</span><span class="sxs-lookup"><span data-stu-id="a7059-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="a7059-129">筆記</span><span class="sxs-lookup"><span data-stu-id="a7059-129">NOTES</span></span>

## <span data-ttu-id="a7059-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="a7059-130">RELATED LINKS</span></span>

[<span data-ttu-id="a7059-131">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a7059-131">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="a7059-132">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a7059-132">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="a7059-133">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a7059-133">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="a7059-134">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a7059-134">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="a7059-135">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a7059-135">Start-AzWebApp</span></span>](./Start-AzWebApp.md)


