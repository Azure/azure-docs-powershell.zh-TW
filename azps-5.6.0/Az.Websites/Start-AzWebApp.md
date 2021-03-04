---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: D70A61D8-0C9A-4BDB-A546-37C32D25797C
online version: https://docs.microsoft.com/powershell/module/az.websites/start-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Start-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Start-AzWebApp.md
ms.openlocfilehash: a05b9ef015d1685e92bc56b0056c9213ff3370ad
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916812"
---
# <span data-ttu-id="b27ff-101">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="b27ff-101">Start-AzWebApp</span></span>

## <span data-ttu-id="b27ff-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b27ff-102">SYNOPSIS</span></span>
<span data-ttu-id="b27ff-103">啟動 Azure Web App。</span><span class="sxs-lookup"><span data-stu-id="b27ff-103">Starts an Azure Web App.</span></span>

## <span data-ttu-id="b27ff-104">語法</span><span class="sxs-lookup"><span data-stu-id="b27ff-104">SYNTAX</span></span>

### <span data-ttu-id="b27ff-105">S1</span><span class="sxs-lookup"><span data-stu-id="b27ff-105">S1</span></span>
```
Start-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b27ff-106">S2</span><span class="sxs-lookup"><span data-stu-id="b27ff-106">S2</span></span>
```
Start-AzWebApp [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b27ff-107">描述</span><span class="sxs-lookup"><span data-stu-id="b27ff-107">DESCRIPTION</span></span>
<span data-ttu-id="b27ff-108">**Start-AzWebApp** Cmdlet 會啟動 Azure Web App。</span><span class="sxs-lookup"><span data-stu-id="b27ff-108">The **Start-AzWebApp** cmdlet starts an Azure Web App.</span></span>

## <span data-ttu-id="b27ff-109">例子</span><span class="sxs-lookup"><span data-stu-id="b27ff-109">EXAMPLES</span></span>

### <span data-ttu-id="b27ff-110">範例 1：啟動 Web App</span><span class="sxs-lookup"><span data-stu-id="b27ff-110">Example 1: Start a Web App</span></span>
```
PS C:\>Start-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="b27ff-111">此命令會啟動名為 ContosoWebApp 的 Web App，該 Web App 屬於名為 Default-Web-WestUS 的資源群組。</span><span class="sxs-lookup"><span data-stu-id="b27ff-111">This command starts the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="b27ff-112">參數</span><span class="sxs-lookup"><span data-stu-id="b27ff-112">PARAMETERS</span></span>

### <span data-ttu-id="b27ff-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b27ff-113">-DefaultProfile</span></span>
<span data-ttu-id="b27ff-114">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b27ff-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b27ff-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="b27ff-115">-Name</span></span>
<span data-ttu-id="b27ff-116">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="b27ff-116">WebApp Name</span></span>

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

### <span data-ttu-id="b27ff-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b27ff-117">-ResourceGroupName</span></span>
<span data-ttu-id="b27ff-118">資源組名</span><span class="sxs-lookup"><span data-stu-id="b27ff-118">Resource Group Name</span></span>

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

### <span data-ttu-id="b27ff-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="b27ff-119">-WebApp</span></span>
<span data-ttu-id="b27ff-120">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="b27ff-120">WebApp Object</span></span>

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

### <span data-ttu-id="b27ff-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b27ff-121">CommonParameters</span></span>
<span data-ttu-id="b27ff-122">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b27ff-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b27ff-123">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="b27ff-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b27ff-124">輸入</span><span class="sxs-lookup"><span data-stu-id="b27ff-124">INPUTS</span></span>

### <span data-ttu-id="b27ff-125">System.String</span><span class="sxs-lookup"><span data-stu-id="b27ff-125">System.String</span></span>

### <span data-ttu-id="b27ff-126">Microsoft.Azure.Commands.WebApps.models.PSSite</span><span class="sxs-lookup"><span data-stu-id="b27ff-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="b27ff-127">輸出</span><span class="sxs-lookup"><span data-stu-id="b27ff-127">OUTPUTS</span></span>

### <span data-ttu-id="b27ff-128">Microsoft.Azure.Commands.WebApps.models.PSSite</span><span class="sxs-lookup"><span data-stu-id="b27ff-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="b27ff-129">筆記</span><span class="sxs-lookup"><span data-stu-id="b27ff-129">NOTES</span></span>

## <span data-ttu-id="b27ff-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="b27ff-130">RELATED LINKS</span></span>

[<span data-ttu-id="b27ff-131">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="b27ff-131">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="b27ff-132">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="b27ff-132">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="b27ff-133">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="b27ff-133">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="b27ff-134">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="b27ff-134">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="b27ff-135">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="b27ff-135">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


