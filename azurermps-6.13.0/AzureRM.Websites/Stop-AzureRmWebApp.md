---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: A12FFDB1-9849-4150-9716-068BE6EFC681
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/stop-azurermwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Stop-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Stop-AzureRmWebApp.md
ms.openlocfilehash: b389a84ea57902e2e7a7dabaea2d853827a728e1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445296"
---
# <span data-ttu-id="c07e9-101">Stop-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="c07e9-101">Stop-AzureRmWebApp</span></span>

## <span data-ttu-id="c07e9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c07e9-102">SYNOPSIS</span></span>
<span data-ttu-id="c07e9-103">停止 Azure Web App。</span><span class="sxs-lookup"><span data-stu-id="c07e9-103">Stops an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c07e9-104">句法</span><span class="sxs-lookup"><span data-stu-id="c07e9-104">SYNTAX</span></span>

### <span data-ttu-id="c07e9-105">S1</span><span class="sxs-lookup"><span data-stu-id="c07e9-105">S1</span></span>
```
Stop-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c07e9-106">S2</span><span class="sxs-lookup"><span data-stu-id="c07e9-106">S2</span></span>
```
Stop-AzureRmWebApp [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c07e9-107">說明</span><span class="sxs-lookup"><span data-stu-id="c07e9-107">DESCRIPTION</span></span>
<span data-ttu-id="c07e9-108">**AzureRmWebApp** Cmdlet 會停止 Azure Web App。</span><span class="sxs-lookup"><span data-stu-id="c07e9-108">The **Stop-AzureRmWebApp** cmdlet stops an Azure Web App.</span></span>

## <span data-ttu-id="c07e9-109">示例</span><span class="sxs-lookup"><span data-stu-id="c07e9-109">EXAMPLES</span></span>

### <span data-ttu-id="c07e9-110">範例1：停止 Web 應用程式</span><span class="sxs-lookup"><span data-stu-id="c07e9-110">Example 1: Stop a Web App</span></span>
```
PS C:\>Stop-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="c07e9-111">這個命令會停止屬於名為「預設-Web-WestUS」資源群組的名為 ContosoWebApp 的 Web App。</span><span class="sxs-lookup"><span data-stu-id="c07e9-111">This command stops the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="c07e9-112">參數</span><span class="sxs-lookup"><span data-stu-id="c07e9-112">PARAMETERS</span></span>

### <span data-ttu-id="c07e9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c07e9-113">-DefaultProfile</span></span>
<span data-ttu-id="c07e9-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c07e9-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c07e9-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="c07e9-115">-Name</span></span>
<span data-ttu-id="c07e9-116">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="c07e9-116">WebApp Name</span></span>

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

### <span data-ttu-id="c07e9-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c07e9-117">-ResourceGroupName</span></span>
<span data-ttu-id="c07e9-118">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="c07e9-118">Resource Group Name</span></span>

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

### <span data-ttu-id="c07e9-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="c07e9-119">-WebApp</span></span>
<span data-ttu-id="c07e9-120">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="c07e9-120">WebApp Object</span></span>

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

### <span data-ttu-id="c07e9-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c07e9-121">CommonParameters</span></span>
<span data-ttu-id="c07e9-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c07e9-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c07e9-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c07e9-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c07e9-124">輸入</span><span class="sxs-lookup"><span data-stu-id="c07e9-124">INPUTS</span></span>

### <span data-ttu-id="c07e9-125">System.object</span><span class="sxs-lookup"><span data-stu-id="c07e9-125">System.String</span></span>

### <span data-ttu-id="c07e9-126">[Microsoft Azure. 管理] 網站</span><span class="sxs-lookup"><span data-stu-id="c07e9-126">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="c07e9-127">參數： WebApp (ByValue) </span><span class="sxs-lookup"><span data-stu-id="c07e9-127">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="c07e9-128">輸出</span><span class="sxs-lookup"><span data-stu-id="c07e9-128">OUTPUTS</span></span>

### <span data-ttu-id="c07e9-129">[Microsoft Azure. 管理] 網站</span><span class="sxs-lookup"><span data-stu-id="c07e9-129">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="c07e9-130">筆記</span><span class="sxs-lookup"><span data-stu-id="c07e9-130">NOTES</span></span>

## <span data-ttu-id="c07e9-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="c07e9-131">RELATED LINKS</span></span>

[<span data-ttu-id="c07e9-132">AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="c07e9-132">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="c07e9-133">新-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="c07e9-133">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="c07e9-134">移除-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="c07e9-134">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="c07e9-135">重新開機-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="c07e9-135">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="c07e9-136">開始-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="c07e9-136">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)


