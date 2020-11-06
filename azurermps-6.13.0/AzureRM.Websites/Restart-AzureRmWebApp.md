---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 297071E5-FC06-4493-BCC2-37D4929E4025
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/restart-azurermwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restart-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restart-AzureRmWebApp.md
ms.openlocfilehash: 42b561707dd1b4240cf0542adfb196250aafc8d1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449663"
---
# <span data-ttu-id="9df49-101">Restart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="9df49-101">Restart-AzureRmWebApp</span></span>

## <span data-ttu-id="9df49-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9df49-102">SYNOPSIS</span></span>
<span data-ttu-id="9df49-103">重新開機 Azure Web App。</span><span class="sxs-lookup"><span data-stu-id="9df49-103">Restarts an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9df49-104">句法</span><span class="sxs-lookup"><span data-stu-id="9df49-104">SYNTAX</span></span>

### <span data-ttu-id="9df49-105">S1</span><span class="sxs-lookup"><span data-stu-id="9df49-105">S1</span></span>
```
Restart-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9df49-106">S2</span><span class="sxs-lookup"><span data-stu-id="9df49-106">S2</span></span>
```
Restart-AzureRmWebApp [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9df49-107">說明</span><span class="sxs-lookup"><span data-stu-id="9df49-107">DESCRIPTION</span></span>
<span data-ttu-id="9df49-108">**Restart AzureRmWebApp** Cmdlet 會停止，然後啟動 Azure Web App。</span><span class="sxs-lookup"><span data-stu-id="9df49-108">The **Restart-AzureRmWebApp** cmdlet stops and then starts an Azure Web App.</span></span>
<span data-ttu-id="9df49-109">如果 Web App 處於停止狀態，請使用 Start-AzureRmWebApp Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9df49-109">If the Web App is in a stopped state, use the Start-AzureRmWebApp cmdlet.</span></span>

## <span data-ttu-id="9df49-110">示例</span><span class="sxs-lookup"><span data-stu-id="9df49-110">EXAMPLES</span></span>

### <span data-ttu-id="9df49-111">範例1：重新開機 Web 應用程式</span><span class="sxs-lookup"><span data-stu-id="9df49-111">Example 1: Restart a Web App</span></span>
```
PS C:\>Restart-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="9df49-112">這個命令會停止名為 ContosoSite 的 Azure Web App，該應用程式屬於名為「預設-Web-WestUS」的資源群組，然後重新開機它。</span><span class="sxs-lookup"><span data-stu-id="9df49-112">This command stops the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS and then restarts it.</span></span>

## <span data-ttu-id="9df49-113">參數</span><span class="sxs-lookup"><span data-stu-id="9df49-113">PARAMETERS</span></span>

### <span data-ttu-id="9df49-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9df49-114">-DefaultProfile</span></span>
<span data-ttu-id="9df49-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9df49-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9df49-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="9df49-116">-Name</span></span>
<span data-ttu-id="9df49-117">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="9df49-117">WebApp Name</span></span>

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

### <span data-ttu-id="9df49-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9df49-118">-ResourceGroupName</span></span>
<span data-ttu-id="9df49-119">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="9df49-119">Resource Group Name</span></span>

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

### <span data-ttu-id="9df49-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="9df49-120">-WebApp</span></span>
<span data-ttu-id="9df49-121">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="9df49-121">WebApp Object</span></span>

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

### <span data-ttu-id="9df49-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9df49-122">CommonParameters</span></span>
<span data-ttu-id="9df49-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9df49-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9df49-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9df49-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9df49-125">輸入</span><span class="sxs-lookup"><span data-stu-id="9df49-125">INPUTS</span></span>

### <span data-ttu-id="9df49-126">System.object</span><span class="sxs-lookup"><span data-stu-id="9df49-126">System.String</span></span>

### <span data-ttu-id="9df49-127">[Microsoft Azure. 管理] 網站</span><span class="sxs-lookup"><span data-stu-id="9df49-127">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="9df49-128">參數： WebApp (ByValue) </span><span class="sxs-lookup"><span data-stu-id="9df49-128">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="9df49-129">輸出</span><span class="sxs-lookup"><span data-stu-id="9df49-129">OUTPUTS</span></span>

### <span data-ttu-id="9df49-130">[Microsoft Azure. 管理] 網站</span><span class="sxs-lookup"><span data-stu-id="9df49-130">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="9df49-131">筆記</span><span class="sxs-lookup"><span data-stu-id="9df49-131">NOTES</span></span>

## <span data-ttu-id="9df49-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="9df49-132">RELATED LINKS</span></span>

[<span data-ttu-id="9df49-133">AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="9df49-133">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="9df49-134">新-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="9df49-134">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="9df49-135">移除-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="9df49-135">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="9df49-136">開始-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="9df49-136">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="9df49-137">停止 AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="9df49-137">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


