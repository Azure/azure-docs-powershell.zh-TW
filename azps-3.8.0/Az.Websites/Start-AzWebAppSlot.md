---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 0FDDDEE1-CEAD-46DA-A7EB-EE477ED59749
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/start-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Start-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Start-AzWebAppSlot.md
ms.openlocfilehash: 4425c344fb0c9e0e3441c172915be11002ee8b1b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958529"
---
# <span data-ttu-id="47610-101">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="47610-101">Start-AzWebAppSlot</span></span>

## <span data-ttu-id="47610-102">摘要</span><span class="sxs-lookup"><span data-stu-id="47610-102">SYNOPSIS</span></span>
<span data-ttu-id="47610-103">啟動 Azure Web App 槽。</span><span class="sxs-lookup"><span data-stu-id="47610-103">Starts an Azure Web App slot.</span></span>

## <span data-ttu-id="47610-104">句法</span><span class="sxs-lookup"><span data-stu-id="47610-104">SYNTAX</span></span>

### <span data-ttu-id="47610-105">S1</span><span class="sxs-lookup"><span data-stu-id="47610-105">S1</span></span>
```
Start-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47610-106">S2</span><span class="sxs-lookup"><span data-stu-id="47610-106">S2</span></span>
```
Start-AzWebAppSlot [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="47610-107">說明</span><span class="sxs-lookup"><span data-stu-id="47610-107">DESCRIPTION</span></span>
<span data-ttu-id="47610-108">**AzWebAppSlot** Cmdlet 會啟動 Azure Web App 槽。</span><span class="sxs-lookup"><span data-stu-id="47610-108">The **Start-AzWebAppSlot** cmdlet starts an Azure Web App Slot.</span></span>

## <span data-ttu-id="47610-109">示例</span><span class="sxs-lookup"><span data-stu-id="47610-109">EXAMPLES</span></span>

### <span data-ttu-id="47610-110">範例1</span><span class="sxs-lookup"><span data-stu-id="47610-110">Example 1</span></span>
```
PS C:\>Start-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="47610-111">這個命令會啟動一個名為 Slot001 的槽，該槽屬於名為 [Default-Web-WestUS] 的資源群組的名為 ContosoWebApp 的 Web App。</span><span class="sxs-lookup"><span data-stu-id="47610-111">This command starts the Slot named Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="47610-112">參數</span><span class="sxs-lookup"><span data-stu-id="47610-112">PARAMETERS</span></span>

### <span data-ttu-id="47610-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47610-113">-DefaultProfile</span></span>
<span data-ttu-id="47610-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="47610-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="47610-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="47610-115">-Name</span></span>
<span data-ttu-id="47610-116">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="47610-116">WebApp Name</span></span>

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

### <span data-ttu-id="47610-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47610-117">-ResourceGroupName</span></span>
<span data-ttu-id="47610-118">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="47610-118">Resource Group Name</span></span>

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

### <span data-ttu-id="47610-119">-槽</span><span class="sxs-lookup"><span data-stu-id="47610-119">-Slot</span></span>
<span data-ttu-id="47610-120">WebApp 槽名稱</span><span class="sxs-lookup"><span data-stu-id="47610-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="47610-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="47610-121">-WebApp</span></span>
<span data-ttu-id="47610-122">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="47610-122">WebApp Object</span></span>

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

### <span data-ttu-id="47610-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47610-123">CommonParameters</span></span>
<span data-ttu-id="47610-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="47610-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47610-125">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="47610-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47610-126">輸入</span><span class="sxs-lookup"><span data-stu-id="47610-126">INPUTS</span></span>

### <span data-ttu-id="47610-127">System.object</span><span class="sxs-lookup"><span data-stu-id="47610-127">System.String</span></span>

### <span data-ttu-id="47610-128">PSSite 中的 WebApps。</span><span class="sxs-lookup"><span data-stu-id="47610-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="47610-129">輸出</span><span class="sxs-lookup"><span data-stu-id="47610-129">OUTPUTS</span></span>

### <span data-ttu-id="47610-130">PSSite 中的 WebApps。</span><span class="sxs-lookup"><span data-stu-id="47610-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="47610-131">筆記</span><span class="sxs-lookup"><span data-stu-id="47610-131">NOTES</span></span>

## <span data-ttu-id="47610-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="47610-132">RELATED LINKS</span></span>

[<span data-ttu-id="47610-133">AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="47610-133">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="47610-134">新-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="47610-134">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="47610-135">移除-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="47610-135">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="47610-136">重新開機-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="47610-136">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="47610-137">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="47610-137">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="47610-138">停止 AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="47610-138">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="47610-139">AzWebApp</span><span class="sxs-lookup"><span data-stu-id="47610-139">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
