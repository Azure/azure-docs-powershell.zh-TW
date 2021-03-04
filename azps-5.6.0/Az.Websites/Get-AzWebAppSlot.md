---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 100A5980-31E2-41F9-84D4-2F5F0CB78B8A
online version: https://docs.microsoft.com/powershell/module/az.websites/get-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlot.md
ms.openlocfilehash: 2f57ba64880f40a411ccac3263fa973815c685f7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917541"
---
# <span data-ttu-id="47568-101">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="47568-101">Get-AzWebAppSlot</span></span>

## <span data-ttu-id="47568-102">簡介</span><span class="sxs-lookup"><span data-stu-id="47568-102">SYNOPSIS</span></span>
<span data-ttu-id="47568-103">獲得 Azure Web App 插槽。</span><span class="sxs-lookup"><span data-stu-id="47568-103">Gets an Azure Web App slot.</span></span>

## <span data-ttu-id="47568-104">語法</span><span class="sxs-lookup"><span data-stu-id="47568-104">SYNTAX</span></span>

### <span data-ttu-id="47568-105">S1</span><span class="sxs-lookup"><span data-stu-id="47568-105">S1</span></span>
```
Get-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47568-106">S2</span><span class="sxs-lookup"><span data-stu-id="47568-106">S2</span></span>
```
Get-AzWebAppSlot [[-Slot] <String>] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="47568-107">描述</span><span class="sxs-lookup"><span data-stu-id="47568-107">DESCRIPTION</span></span>
<span data-ttu-id="47568-108">**Get-AzWebAppSlot** Cmdlet 會取得 Azure Web App Slot 相關資訊。</span><span class="sxs-lookup"><span data-stu-id="47568-108">The **Get-AzWebAppSlot** cmdlet gets information about an Azure Web App Slot.</span></span>

## <span data-ttu-id="47568-109">例子</span><span class="sxs-lookup"><span data-stu-id="47568-109">EXAMPLES</span></span>

### <span data-ttu-id="47568-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="47568-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -Slot "Slot001"
```

<span data-ttu-id="47568-111">此命令會從名稱為 WebAppStandard 的 Web App 中，從屬於 Default-Web-WestUS 的資源群組中，獲得名為 Slot001 的插槽。</span><span class="sxs-lookup"><span data-stu-id="47568-111">This command gets the slot named Slot001 from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="47568-112">參數</span><span class="sxs-lookup"><span data-stu-id="47568-112">PARAMETERS</span></span>

### <span data-ttu-id="47568-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47568-113">-DefaultProfile</span></span>
<span data-ttu-id="47568-114">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="47568-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="47568-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="47568-115">-Name</span></span>
<span data-ttu-id="47568-116">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="47568-116">WebApp Name</span></span>

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

### <span data-ttu-id="47568-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47568-117">-ResourceGroupName</span></span>
<span data-ttu-id="47568-118">資源組名</span><span class="sxs-lookup"><span data-stu-id="47568-118">Resource Group Name</span></span>

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

### <span data-ttu-id="47568-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="47568-119">-Slot</span></span>
<span data-ttu-id="47568-120">WebApp Slot 名稱</span><span class="sxs-lookup"><span data-stu-id="47568-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="47568-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="47568-121">-WebApp</span></span>
<span data-ttu-id="47568-122">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="47568-122">WebApp Object</span></span>

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

### <span data-ttu-id="47568-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47568-123">CommonParameters</span></span>
<span data-ttu-id="47568-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="47568-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47568-125">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="47568-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47568-126">輸入</span><span class="sxs-lookup"><span data-stu-id="47568-126">INPUTS</span></span>

### <span data-ttu-id="47568-127">System.String</span><span class="sxs-lookup"><span data-stu-id="47568-127">System.String</span></span>

### <span data-ttu-id="47568-128">Microsoft.Azure.Commands.WebApps.models.PSSite</span><span class="sxs-lookup"><span data-stu-id="47568-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="47568-129">輸出</span><span class="sxs-lookup"><span data-stu-id="47568-129">OUTPUTS</span></span>

### <span data-ttu-id="47568-130">Microsoft.Azure.Commands.WebApps.models.PSSite</span><span class="sxs-lookup"><span data-stu-id="47568-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="47568-131">筆記</span><span class="sxs-lookup"><span data-stu-id="47568-131">NOTES</span></span>

## <span data-ttu-id="47568-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="47568-132">RELATED LINKS</span></span>

[<span data-ttu-id="47568-133">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="47568-133">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="47568-134">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="47568-134">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="47568-135">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="47568-135">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="47568-136">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="47568-136">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="47568-137">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="47568-137">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="47568-138">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="47568-138">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="47568-139">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="47568-139">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
