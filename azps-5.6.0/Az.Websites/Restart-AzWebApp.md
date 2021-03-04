---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 297071E5-FC06-4493-BCC2-37D4929E4025
online version: https://docs.microsoft.com/powershell/module/az.websites/restart-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restart-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restart-AzWebApp.md
ms.openlocfilehash: e155a58420d9f190bfebdb21272d64dab1f3c21f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914978"
---
# <span data-ttu-id="ce39c-101">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ce39c-101">Restart-AzWebApp</span></span>

## <span data-ttu-id="ce39c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ce39c-102">SYNOPSIS</span></span>
<span data-ttu-id="ce39c-103">重新開機 Azure Web App。</span><span class="sxs-lookup"><span data-stu-id="ce39c-103">Restarts an Azure Web App.</span></span>

## <span data-ttu-id="ce39c-104">語法</span><span class="sxs-lookup"><span data-stu-id="ce39c-104">SYNTAX</span></span>

### <span data-ttu-id="ce39c-105">S1</span><span class="sxs-lookup"><span data-stu-id="ce39c-105">S1</span></span>
```
Restart-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ce39c-106">S2</span><span class="sxs-lookup"><span data-stu-id="ce39c-106">S2</span></span>
```
Restart-AzWebApp [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ce39c-107">描述</span><span class="sxs-lookup"><span data-stu-id="ce39c-107">DESCRIPTION</span></span>
<span data-ttu-id="ce39c-108">**Restart-AzWebApp** Cmdlet 會停止，然後啟動 Azure Web App。</span><span class="sxs-lookup"><span data-stu-id="ce39c-108">The **Restart-AzWebApp** cmdlet stops and then starts an Azure Web App.</span></span>
<span data-ttu-id="ce39c-109">如果 Web App 已停止，請使用 Start-AzWebApp Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ce39c-109">If the Web App is in a stopped state, use the Start-AzWebApp cmdlet.</span></span>

## <span data-ttu-id="ce39c-110">例子</span><span class="sxs-lookup"><span data-stu-id="ce39c-110">EXAMPLES</span></span>

### <span data-ttu-id="ce39c-111">範例 1：重新開機 Web App</span><span class="sxs-lookup"><span data-stu-id="ce39c-111">Example 1: Restart a Web App</span></span>
```
PS C:\>Restart-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="ce39c-112">此命令會停止名稱為 ContosoSite 的 Azure Web App，此 App 屬於 Default-Web-WestUS 資源群組，然後重新開機。</span><span class="sxs-lookup"><span data-stu-id="ce39c-112">This command stops the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS and then restarts it.</span></span>

## <span data-ttu-id="ce39c-113">參數</span><span class="sxs-lookup"><span data-stu-id="ce39c-113">PARAMETERS</span></span>

### <span data-ttu-id="ce39c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce39c-114">-DefaultProfile</span></span>
<span data-ttu-id="ce39c-115">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ce39c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ce39c-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="ce39c-116">-Name</span></span>
<span data-ttu-id="ce39c-117">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="ce39c-117">WebApp Name</span></span>

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

### <span data-ttu-id="ce39c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce39c-118">-ResourceGroupName</span></span>
<span data-ttu-id="ce39c-119">資源組名</span><span class="sxs-lookup"><span data-stu-id="ce39c-119">Resource Group Name</span></span>

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

### <span data-ttu-id="ce39c-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="ce39c-120">-WebApp</span></span>
<span data-ttu-id="ce39c-121">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="ce39c-121">WebApp Object</span></span>

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

### <span data-ttu-id="ce39c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce39c-122">CommonParameters</span></span>
<span data-ttu-id="ce39c-123">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ce39c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce39c-124">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="ce39c-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce39c-125">輸入</span><span class="sxs-lookup"><span data-stu-id="ce39c-125">INPUTS</span></span>

### <span data-ttu-id="ce39c-126">System.String</span><span class="sxs-lookup"><span data-stu-id="ce39c-126">System.String</span></span>

### <span data-ttu-id="ce39c-127">Microsoft.Azure.Commands.WebApps.models.PSSite</span><span class="sxs-lookup"><span data-stu-id="ce39c-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="ce39c-128">輸出</span><span class="sxs-lookup"><span data-stu-id="ce39c-128">OUTPUTS</span></span>

### <span data-ttu-id="ce39c-129">Microsoft.Azure.Commands.WebApps.models.PSSite</span><span class="sxs-lookup"><span data-stu-id="ce39c-129">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="ce39c-130">筆記</span><span class="sxs-lookup"><span data-stu-id="ce39c-130">NOTES</span></span>

## <span data-ttu-id="ce39c-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="ce39c-131">RELATED LINKS</span></span>

[<span data-ttu-id="ce39c-132">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ce39c-132">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="ce39c-133">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ce39c-133">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="ce39c-134">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ce39c-134">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="ce39c-135">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ce39c-135">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="ce39c-136">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ce39c-136">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


