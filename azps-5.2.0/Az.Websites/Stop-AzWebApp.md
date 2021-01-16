---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: A12FFDB1-9849-4150-9716-068BE6EFC681
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/stop-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Stop-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Stop-AzWebApp.md
ms.openlocfilehash: d08303ec0057a42569455c9e52c38e561de73e4d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98280407"
---
# <span data-ttu-id="3b3c4-101">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="3b3c4-101">Stop-AzWebApp</span></span>

## <span data-ttu-id="3b3c4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3b3c4-102">SYNOPSIS</span></span>
<span data-ttu-id="3b3c4-103">停止 Azure Web App。</span><span class="sxs-lookup"><span data-stu-id="3b3c4-103">Stops an Azure Web App.</span></span>

## <span data-ttu-id="3b3c4-104">句法</span><span class="sxs-lookup"><span data-stu-id="3b3c4-104">SYNTAX</span></span>

### <span data-ttu-id="3b3c4-105">S1</span><span class="sxs-lookup"><span data-stu-id="3b3c4-105">S1</span></span>
```
Stop-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3b3c4-106">S2</span><span class="sxs-lookup"><span data-stu-id="3b3c4-106">S2</span></span>
```
Stop-AzWebApp [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3b3c4-107">說明</span><span class="sxs-lookup"><span data-stu-id="3b3c4-107">DESCRIPTION</span></span>
<span data-ttu-id="3b3c4-108">**AzWebApp** Cmdlet 會停止 Azure Web App。</span><span class="sxs-lookup"><span data-stu-id="3b3c4-108">The **Stop-AzWebApp** cmdlet stops an Azure Web App.</span></span>

## <span data-ttu-id="3b3c4-109">示例</span><span class="sxs-lookup"><span data-stu-id="3b3c4-109">EXAMPLES</span></span>

### <span data-ttu-id="3b3c4-110">範例1：停止 Web 應用程式</span><span class="sxs-lookup"><span data-stu-id="3b3c4-110">Example 1: Stop a Web App</span></span>
```
PS C:\>Stop-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="3b3c4-111">這個命令會停止屬於名為「預設-Web-WestUS」資源群組的名為 ContosoWebApp 的 Web App。</span><span class="sxs-lookup"><span data-stu-id="3b3c4-111">This command stops the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="3b3c4-112">參數</span><span class="sxs-lookup"><span data-stu-id="3b3c4-112">PARAMETERS</span></span>

### <span data-ttu-id="3b3c4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b3c4-113">-DefaultProfile</span></span>
<span data-ttu-id="3b3c4-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3b3c4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3b3c4-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="3b3c4-115">-Name</span></span>
<span data-ttu-id="3b3c4-116">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="3b3c4-116">WebApp Name</span></span>

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

### <span data-ttu-id="3b3c4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b3c4-117">-ResourceGroupName</span></span>
<span data-ttu-id="3b3c4-118">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="3b3c4-118">Resource Group Name</span></span>

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

### <span data-ttu-id="3b3c4-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="3b3c4-119">-WebApp</span></span>
<span data-ttu-id="3b3c4-120">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="3b3c4-120">WebApp Object</span></span>

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

### <span data-ttu-id="3b3c4-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b3c4-121">CommonParameters</span></span>
<span data-ttu-id="3b3c4-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3b3c4-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b3c4-123">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3b3c4-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b3c4-124">輸入</span><span class="sxs-lookup"><span data-stu-id="3b3c4-124">INPUTS</span></span>

### <span data-ttu-id="3b3c4-125">System.object</span><span class="sxs-lookup"><span data-stu-id="3b3c4-125">System.String</span></span>

### <span data-ttu-id="3b3c4-126">PSSite 中的 WebApps。</span><span class="sxs-lookup"><span data-stu-id="3b3c4-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="3b3c4-127">輸出</span><span class="sxs-lookup"><span data-stu-id="3b3c4-127">OUTPUTS</span></span>

### <span data-ttu-id="3b3c4-128">PSSite 中的 WebApps。</span><span class="sxs-lookup"><span data-stu-id="3b3c4-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="3b3c4-129">筆記</span><span class="sxs-lookup"><span data-stu-id="3b3c4-129">NOTES</span></span>

## <span data-ttu-id="3b3c4-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="3b3c4-130">RELATED LINKS</span></span>

[<span data-ttu-id="3b3c4-131">AzWebApp</span><span class="sxs-lookup"><span data-stu-id="3b3c4-131">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="3b3c4-132">新-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="3b3c4-132">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="3b3c4-133">移除-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="3b3c4-133">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="3b3c4-134">重新開機-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="3b3c4-134">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="3b3c4-135">開始-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="3b3c4-135">Start-AzWebApp</span></span>](./Start-AzWebApp.md)


