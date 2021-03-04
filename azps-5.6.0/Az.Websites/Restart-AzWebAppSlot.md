---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 645E74D2-640D-494F-9798-4375FE6A0AF2
online version: https://docs.microsoft.com/powershell/module/az.websites/restart-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restart-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restart-AzWebAppSlot.md
ms.openlocfilehash: 75bedf4546bee73767c0488f578cdb5e17c1b745
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914974"
---
# <span data-ttu-id="4b293-101">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="4b293-101">Restart-AzWebAppSlot</span></span>

## <span data-ttu-id="4b293-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4b293-102">SYNOPSIS</span></span>

## <span data-ttu-id="4b293-103">語法</span><span class="sxs-lookup"><span data-stu-id="4b293-103">SYNTAX</span></span>

### <span data-ttu-id="4b293-104">S1</span><span class="sxs-lookup"><span data-stu-id="4b293-104">S1</span></span>
```
Restart-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4b293-105">S2</span><span class="sxs-lookup"><span data-stu-id="4b293-105">S2</span></span>
```
Restart-AzWebAppSlot [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4b293-106">描述</span><span class="sxs-lookup"><span data-stu-id="4b293-106">DESCRIPTION</span></span>
<span data-ttu-id="4b293-107">**Restart-AzWebAppSlot** Cmdlet 會停止，然後啟動 Azure Web App Slot。</span><span class="sxs-lookup"><span data-stu-id="4b293-107">The **Restart-AzWebAppSlot** cmdlet stops and then starts an Azure Web App Slot.</span></span>
<span data-ttu-id="4b293-108">如果 Web App Slot 已停止，請使用 Start-AzWebAppSlot Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4b293-108">If the Web App Slot is in a stopped state, use the Start-AzWebAppSlot cmdlet.</span></span>

## <span data-ttu-id="4b293-109">例子</span><span class="sxs-lookup"><span data-stu-id="4b293-109">EXAMPLES</span></span>

### <span data-ttu-id="4b293-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="4b293-110">Example 1</span></span>
```
PS C:\> Restart-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="4b293-111">此命令會重新開機與資源群組 Default-Web-WestUS 相關聯的 Web App ContosoWebApp 插槽 Slot001</span><span class="sxs-lookup"><span data-stu-id="4b293-111">This command restarts the slot Slot001 for the web app ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="4b293-112">參數</span><span class="sxs-lookup"><span data-stu-id="4b293-112">PARAMETERS</span></span>

### <span data-ttu-id="4b293-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b293-113">-DefaultProfile</span></span>
<span data-ttu-id="4b293-114">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="4b293-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4b293-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="4b293-115">-Name</span></span>
<span data-ttu-id="4b293-116">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="4b293-116">WebApp Name</span></span>

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

### <span data-ttu-id="4b293-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b293-117">-ResourceGroupName</span></span>
<span data-ttu-id="4b293-118">資源組名</span><span class="sxs-lookup"><span data-stu-id="4b293-118">Resource Group Name</span></span>

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

### <span data-ttu-id="4b293-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="4b293-119">-Slot</span></span>
<span data-ttu-id="4b293-120">WebApp Slot 名稱</span><span class="sxs-lookup"><span data-stu-id="4b293-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="4b293-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="4b293-121">-WebApp</span></span>
<span data-ttu-id="4b293-122">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="4b293-122">WebApp Object</span></span>

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

### <span data-ttu-id="4b293-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b293-123">CommonParameters</span></span>
<span data-ttu-id="4b293-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4b293-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b293-125">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="4b293-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b293-126">輸入</span><span class="sxs-lookup"><span data-stu-id="4b293-126">INPUTS</span></span>

### <span data-ttu-id="4b293-127">System.String</span><span class="sxs-lookup"><span data-stu-id="4b293-127">System.String</span></span>

### <span data-ttu-id="4b293-128">Microsoft.Azure.Commands.WebApps.models.PSSite</span><span class="sxs-lookup"><span data-stu-id="4b293-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="4b293-129">輸出</span><span class="sxs-lookup"><span data-stu-id="4b293-129">OUTPUTS</span></span>

### <span data-ttu-id="4b293-130">Microsoft.Azure.Commands.WebApps.models.PSSite</span><span class="sxs-lookup"><span data-stu-id="4b293-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="4b293-131">筆記</span><span class="sxs-lookup"><span data-stu-id="4b293-131">NOTES</span></span>

## <span data-ttu-id="4b293-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="4b293-132">RELATED LINKS</span></span>

[<span data-ttu-id="4b293-133">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="4b293-133">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="4b293-134">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="4b293-134">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="4b293-135">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="4b293-135">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="4b293-136">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="4b293-136">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="4b293-137">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="4b293-137">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="4b293-138">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="4b293-138">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="4b293-139">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="4b293-139">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
