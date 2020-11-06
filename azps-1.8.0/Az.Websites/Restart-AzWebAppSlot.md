---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 645E74D2-640D-494F-9798-4375FE6A0AF2
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/restart-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restart-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restart-AzWebAppSlot.md
ms.openlocfilehash: 53323aaf29145f4340dd00fa752d8afd2dd72131
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93614248"
---
# <span data-ttu-id="0119d-101">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="0119d-101">Restart-AzWebAppSlot</span></span>

## <span data-ttu-id="0119d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0119d-102">SYNOPSIS</span></span>

## <span data-ttu-id="0119d-103">句法</span><span class="sxs-lookup"><span data-stu-id="0119d-103">SYNTAX</span></span>

### <span data-ttu-id="0119d-104">S1</span><span class="sxs-lookup"><span data-stu-id="0119d-104">S1</span></span>
```
Restart-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0119d-105">S2</span><span class="sxs-lookup"><span data-stu-id="0119d-105">S2</span></span>
```
Restart-AzWebAppSlot [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0119d-106">說明</span><span class="sxs-lookup"><span data-stu-id="0119d-106">DESCRIPTION</span></span>
<span data-ttu-id="0119d-107">**Restart AzWebAppSlot** Cmdlet 會停止，然後啟動 Azure Web App 槽。</span><span class="sxs-lookup"><span data-stu-id="0119d-107">The **Restart-AzWebAppSlot** cmdlet stops and then starts an Azure Web App Slot.</span></span>
<span data-ttu-id="0119d-108">如果 Web 應用程式槽處於停止狀態，請使用 Start-AzWebAppSlot Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0119d-108">If the Web App Slot is in a stopped state, use the Start-AzWebAppSlot cmdlet.</span></span>

## <span data-ttu-id="0119d-109">示例</span><span class="sxs-lookup"><span data-stu-id="0119d-109">EXAMPLES</span></span>

### <span data-ttu-id="0119d-110">範例1</span><span class="sxs-lookup"><span data-stu-id="0119d-110">Example 1</span></span>
```
PS C:\> Restart-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="0119d-111">這個命令會重新開機與資源群組 Slot001 相關聯之 web app ContosoWebApp 的槽，其預設為 Web-WestUS</span><span class="sxs-lookup"><span data-stu-id="0119d-111">This command restarts the slot Slot001 for the web app ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="0119d-112">參數</span><span class="sxs-lookup"><span data-stu-id="0119d-112">PARAMETERS</span></span>

### <span data-ttu-id="0119d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0119d-113">-DefaultProfile</span></span>
<span data-ttu-id="0119d-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0119d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0119d-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="0119d-115">-Name</span></span>
<span data-ttu-id="0119d-116">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="0119d-116">WebApp Name</span></span>

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

### <span data-ttu-id="0119d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0119d-117">-ResourceGroupName</span></span>
<span data-ttu-id="0119d-118">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="0119d-118">Resource Group Name</span></span>

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

### <span data-ttu-id="0119d-119">-槽</span><span class="sxs-lookup"><span data-stu-id="0119d-119">-Slot</span></span>
<span data-ttu-id="0119d-120">WebApp 槽名稱</span><span class="sxs-lookup"><span data-stu-id="0119d-120">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0119d-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="0119d-121">-WebApp</span></span>
<span data-ttu-id="0119d-122">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="0119d-122">WebApp Object</span></span>

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

### <span data-ttu-id="0119d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0119d-123">CommonParameters</span></span>
<span data-ttu-id="0119d-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0119d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0119d-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0119d-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0119d-126">輸入</span><span class="sxs-lookup"><span data-stu-id="0119d-126">INPUTS</span></span>

### <span data-ttu-id="0119d-127">System.object</span><span class="sxs-lookup"><span data-stu-id="0119d-127">System.String</span></span>

### <span data-ttu-id="0119d-128">PSSite 中的 WebApps。</span><span class="sxs-lookup"><span data-stu-id="0119d-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="0119d-129">輸出</span><span class="sxs-lookup"><span data-stu-id="0119d-129">OUTPUTS</span></span>

### <span data-ttu-id="0119d-130">PSSite 中的 WebApps。</span><span class="sxs-lookup"><span data-stu-id="0119d-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="0119d-131">筆記</span><span class="sxs-lookup"><span data-stu-id="0119d-131">NOTES</span></span>

## <span data-ttu-id="0119d-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="0119d-132">RELATED LINKS</span></span>

[<span data-ttu-id="0119d-133">AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="0119d-133">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="0119d-134">新-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="0119d-134">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="0119d-135">移除-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="0119d-135">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="0119d-136">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="0119d-136">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="0119d-137">開始-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="0119d-137">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="0119d-138">停止 AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="0119d-138">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="0119d-139">AzWebApp</span><span class="sxs-lookup"><span data-stu-id="0119d-139">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
