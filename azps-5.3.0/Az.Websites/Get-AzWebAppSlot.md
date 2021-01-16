---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 100A5980-31E2-41F9-84D4-2F5F0CB78B8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlot.md
ms.openlocfilehash: 4bd0e45df7f1c5c98b61f7f490a59a4c305c2c21
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98436014"
---
# <span data-ttu-id="cce6e-101">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="cce6e-101">Get-AzWebAppSlot</span></span>

## <span data-ttu-id="cce6e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cce6e-102">SYNOPSIS</span></span>
<span data-ttu-id="cce6e-103">取得 Azure Web App 槽。</span><span class="sxs-lookup"><span data-stu-id="cce6e-103">Gets an Azure Web App slot.</span></span>

## <span data-ttu-id="cce6e-104">句法</span><span class="sxs-lookup"><span data-stu-id="cce6e-104">SYNTAX</span></span>

### <span data-ttu-id="cce6e-105">S1</span><span class="sxs-lookup"><span data-stu-id="cce6e-105">S1</span></span>
```
Get-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cce6e-106">S2</span><span class="sxs-lookup"><span data-stu-id="cce6e-106">S2</span></span>
```
Get-AzWebAppSlot [[-Slot] <String>] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cce6e-107">說明</span><span class="sxs-lookup"><span data-stu-id="cce6e-107">DESCRIPTION</span></span>
<span data-ttu-id="cce6e-108">**AzWebAppSlot** Cmdlet 會取得 Azure Web App 槽的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="cce6e-108">The **Get-AzWebAppSlot** cmdlet gets information about an Azure Web App Slot.</span></span>

## <span data-ttu-id="cce6e-109">示例</span><span class="sxs-lookup"><span data-stu-id="cce6e-109">EXAMPLES</span></span>

### <span data-ttu-id="cce6e-110">範例1</span><span class="sxs-lookup"><span data-stu-id="cce6e-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -Slot "Slot001"
```

<span data-ttu-id="cce6e-111">這個命令會從屬於資源群組 Default-Web-WestUS 之名為 WebAppStandard 的 Web App 取得名為 Slot001 的槽。</span><span class="sxs-lookup"><span data-stu-id="cce6e-111">This command gets the slot named Slot001 from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="cce6e-112">參數</span><span class="sxs-lookup"><span data-stu-id="cce6e-112">PARAMETERS</span></span>

### <span data-ttu-id="cce6e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cce6e-113">-DefaultProfile</span></span>
<span data-ttu-id="cce6e-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cce6e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cce6e-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="cce6e-115">-Name</span></span>
<span data-ttu-id="cce6e-116">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="cce6e-116">WebApp Name</span></span>

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

### <span data-ttu-id="cce6e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cce6e-117">-ResourceGroupName</span></span>
<span data-ttu-id="cce6e-118">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="cce6e-118">Resource Group Name</span></span>

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

### <span data-ttu-id="cce6e-119">-槽</span><span class="sxs-lookup"><span data-stu-id="cce6e-119">-Slot</span></span>
<span data-ttu-id="cce6e-120">WebApp 槽名稱</span><span class="sxs-lookup"><span data-stu-id="cce6e-120">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cce6e-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="cce6e-121">-WebApp</span></span>
<span data-ttu-id="cce6e-122">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="cce6e-122">WebApp Object</span></span>

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

### <span data-ttu-id="cce6e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cce6e-123">CommonParameters</span></span>
<span data-ttu-id="cce6e-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cce6e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cce6e-125">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cce6e-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cce6e-126">輸入</span><span class="sxs-lookup"><span data-stu-id="cce6e-126">INPUTS</span></span>

### <span data-ttu-id="cce6e-127">System.object</span><span class="sxs-lookup"><span data-stu-id="cce6e-127">System.String</span></span>

### <span data-ttu-id="cce6e-128">PSSite 中的 WebApps。</span><span class="sxs-lookup"><span data-stu-id="cce6e-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="cce6e-129">輸出</span><span class="sxs-lookup"><span data-stu-id="cce6e-129">OUTPUTS</span></span>

### <span data-ttu-id="cce6e-130">PSSite 中的 WebApps。</span><span class="sxs-lookup"><span data-stu-id="cce6e-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="cce6e-131">筆記</span><span class="sxs-lookup"><span data-stu-id="cce6e-131">NOTES</span></span>

## <span data-ttu-id="cce6e-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="cce6e-132">RELATED LINKS</span></span>

[<span data-ttu-id="cce6e-133">新-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="cce6e-133">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="cce6e-134">移除-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="cce6e-134">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="cce6e-135">重新開機-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="cce6e-135">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="cce6e-136">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="cce6e-136">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="cce6e-137">開始-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="cce6e-137">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="cce6e-138">停止 AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="cce6e-138">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="cce6e-139">AzWebApp</span><span class="sxs-lookup"><span data-stu-id="cce6e-139">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
