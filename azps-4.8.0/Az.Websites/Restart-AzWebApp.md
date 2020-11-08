---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 297071E5-FC06-4493-BCC2-37D4929E4025
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/restart-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restart-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restart-AzWebApp.md
ms.openlocfilehash: faa3264dbf9fa65a2970f578c635868d185f2ef8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94126643"
---
# <span data-ttu-id="dec51-101">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="dec51-101">Restart-AzWebApp</span></span>

## <span data-ttu-id="dec51-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dec51-102">SYNOPSIS</span></span>
<span data-ttu-id="dec51-103">重新開機 Azure Web App。</span><span class="sxs-lookup"><span data-stu-id="dec51-103">Restarts an Azure Web App.</span></span>

## <span data-ttu-id="dec51-104">句法</span><span class="sxs-lookup"><span data-stu-id="dec51-104">SYNTAX</span></span>

### <span data-ttu-id="dec51-105">S1</span><span class="sxs-lookup"><span data-stu-id="dec51-105">S1</span></span>
```
Restart-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dec51-106">S2</span><span class="sxs-lookup"><span data-stu-id="dec51-106">S2</span></span>
```
Restart-AzWebApp [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dec51-107">說明</span><span class="sxs-lookup"><span data-stu-id="dec51-107">DESCRIPTION</span></span>
<span data-ttu-id="dec51-108">**Restart AzWebApp** Cmdlet 會停止，然後啟動 Azure Web App。</span><span class="sxs-lookup"><span data-stu-id="dec51-108">The **Restart-AzWebApp** cmdlet stops and then starts an Azure Web App.</span></span>
<span data-ttu-id="dec51-109">如果 Web App 處於停止狀態，請使用 Start-AzWebApp Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="dec51-109">If the Web App is in a stopped state, use the Start-AzWebApp cmdlet.</span></span>

## <span data-ttu-id="dec51-110">示例</span><span class="sxs-lookup"><span data-stu-id="dec51-110">EXAMPLES</span></span>

### <span data-ttu-id="dec51-111">範例1：重新開機 Web 應用程式</span><span class="sxs-lookup"><span data-stu-id="dec51-111">Example 1: Restart a Web App</span></span>
```
PS C:\>Restart-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="dec51-112">這個命令會停止名為 ContosoSite 的 Azure Web App，該應用程式屬於名為「預設-Web-WestUS」的資源群組，然後重新開機它。</span><span class="sxs-lookup"><span data-stu-id="dec51-112">This command stops the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS and then restarts it.</span></span>

## <span data-ttu-id="dec51-113">參數</span><span class="sxs-lookup"><span data-stu-id="dec51-113">PARAMETERS</span></span>

### <span data-ttu-id="dec51-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dec51-114">-DefaultProfile</span></span>
<span data-ttu-id="dec51-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="dec51-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dec51-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="dec51-116">-Name</span></span>
<span data-ttu-id="dec51-117">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="dec51-117">WebApp Name</span></span>

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

### <span data-ttu-id="dec51-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dec51-118">-ResourceGroupName</span></span>
<span data-ttu-id="dec51-119">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="dec51-119">Resource Group Name</span></span>

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

### <span data-ttu-id="dec51-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="dec51-120">-WebApp</span></span>
<span data-ttu-id="dec51-121">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="dec51-121">WebApp Object</span></span>

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

### <span data-ttu-id="dec51-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dec51-122">CommonParameters</span></span>
<span data-ttu-id="dec51-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dec51-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dec51-124">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="dec51-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dec51-125">輸入</span><span class="sxs-lookup"><span data-stu-id="dec51-125">INPUTS</span></span>

### <span data-ttu-id="dec51-126">System.object</span><span class="sxs-lookup"><span data-stu-id="dec51-126">System.String</span></span>

### <span data-ttu-id="dec51-127">PSSite 中的 WebApps。</span><span class="sxs-lookup"><span data-stu-id="dec51-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="dec51-128">輸出</span><span class="sxs-lookup"><span data-stu-id="dec51-128">OUTPUTS</span></span>

### <span data-ttu-id="dec51-129">PSSite 中的 WebApps。</span><span class="sxs-lookup"><span data-stu-id="dec51-129">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="dec51-130">筆記</span><span class="sxs-lookup"><span data-stu-id="dec51-130">NOTES</span></span>

## <span data-ttu-id="dec51-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="dec51-131">RELATED LINKS</span></span>

[<span data-ttu-id="dec51-132">AzWebApp</span><span class="sxs-lookup"><span data-stu-id="dec51-132">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="dec51-133">新-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="dec51-133">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="dec51-134">移除-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="dec51-134">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="dec51-135">開始-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="dec51-135">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="dec51-136">停止 AzWebApp</span><span class="sxs-lookup"><span data-stu-id="dec51-136">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


