---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: D70A61D8-0C9A-4BDB-A546-37C32D25797C
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/start-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Start-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Start-AzWebApp.md
ms.openlocfilehash: 33fdfdc1c8b0c4b7bfddbc6b0aafd9ab38ffe701
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98435951"
---
# <span data-ttu-id="c179a-101">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c179a-101">Start-AzWebApp</span></span>

## <span data-ttu-id="c179a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c179a-102">SYNOPSIS</span></span>
<span data-ttu-id="c179a-103">啟動 Azure Web App。</span><span class="sxs-lookup"><span data-stu-id="c179a-103">Starts an Azure Web App.</span></span>

## <span data-ttu-id="c179a-104">句法</span><span class="sxs-lookup"><span data-stu-id="c179a-104">SYNTAX</span></span>

### <span data-ttu-id="c179a-105">S1</span><span class="sxs-lookup"><span data-stu-id="c179a-105">S1</span></span>
```
Start-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c179a-106">S2</span><span class="sxs-lookup"><span data-stu-id="c179a-106">S2</span></span>
```
Start-AzWebApp [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c179a-107">說明</span><span class="sxs-lookup"><span data-stu-id="c179a-107">DESCRIPTION</span></span>
<span data-ttu-id="c179a-108">**AzWebApp** Cmdlet 會啟動 Azure Web App。</span><span class="sxs-lookup"><span data-stu-id="c179a-108">The **Start-AzWebApp** cmdlet starts an Azure Web App.</span></span>

## <span data-ttu-id="c179a-109">示例</span><span class="sxs-lookup"><span data-stu-id="c179a-109">EXAMPLES</span></span>

### <span data-ttu-id="c179a-110">範例1：啟動 Web 應用程式</span><span class="sxs-lookup"><span data-stu-id="c179a-110">Example 1: Start a Web App</span></span>
```
PS C:\>Start-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="c179a-111">這個命令會啟動名為 ContosoWebApp 的 Web App，該應用程式屬於名為「預設-Web-WestUS」的資源群組。</span><span class="sxs-lookup"><span data-stu-id="c179a-111">This command starts the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="c179a-112">參數</span><span class="sxs-lookup"><span data-stu-id="c179a-112">PARAMETERS</span></span>

### <span data-ttu-id="c179a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c179a-113">-DefaultProfile</span></span>
<span data-ttu-id="c179a-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c179a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c179a-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="c179a-115">-Name</span></span>
<span data-ttu-id="c179a-116">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="c179a-116">WebApp Name</span></span>

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

### <span data-ttu-id="c179a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c179a-117">-ResourceGroupName</span></span>
<span data-ttu-id="c179a-118">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="c179a-118">Resource Group Name</span></span>

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

### <span data-ttu-id="c179a-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="c179a-119">-WebApp</span></span>
<span data-ttu-id="c179a-120">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="c179a-120">WebApp Object</span></span>

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

### <span data-ttu-id="c179a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c179a-121">CommonParameters</span></span>
<span data-ttu-id="c179a-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c179a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c179a-123">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c179a-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c179a-124">輸入</span><span class="sxs-lookup"><span data-stu-id="c179a-124">INPUTS</span></span>

### <span data-ttu-id="c179a-125">System.object</span><span class="sxs-lookup"><span data-stu-id="c179a-125">System.String</span></span>

### <span data-ttu-id="c179a-126">PSSite 中的 WebApps。</span><span class="sxs-lookup"><span data-stu-id="c179a-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="c179a-127">輸出</span><span class="sxs-lookup"><span data-stu-id="c179a-127">OUTPUTS</span></span>

### <span data-ttu-id="c179a-128">PSSite 中的 WebApps。</span><span class="sxs-lookup"><span data-stu-id="c179a-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="c179a-129">筆記</span><span class="sxs-lookup"><span data-stu-id="c179a-129">NOTES</span></span>

## <span data-ttu-id="c179a-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="c179a-130">RELATED LINKS</span></span>

[<span data-ttu-id="c179a-131">AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c179a-131">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="c179a-132">新-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c179a-132">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="c179a-133">移除-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c179a-133">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="c179a-134">重新開機-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c179a-134">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="c179a-135">停止 AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c179a-135">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


