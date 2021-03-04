---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 0FDDDEE1-CEAD-46DA-A7EB-EE477ED59749
online version: https://docs.microsoft.com/powershell/module/az.websites/start-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Start-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Start-AzWebAppSlot.md
ms.openlocfilehash: c65eac94a9c44b3b7272116bc0e0757291b121b8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916810"
---
# <span data-ttu-id="26600-101">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="26600-101">Start-AzWebAppSlot</span></span>

## <span data-ttu-id="26600-102">簡介</span><span class="sxs-lookup"><span data-stu-id="26600-102">SYNOPSIS</span></span>
<span data-ttu-id="26600-103">啟動 Azure Web App 插槽。</span><span class="sxs-lookup"><span data-stu-id="26600-103">Starts an Azure Web App slot.</span></span>

## <span data-ttu-id="26600-104">語法</span><span class="sxs-lookup"><span data-stu-id="26600-104">SYNTAX</span></span>

### <span data-ttu-id="26600-105">S1</span><span class="sxs-lookup"><span data-stu-id="26600-105">S1</span></span>
```
Start-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="26600-106">S2</span><span class="sxs-lookup"><span data-stu-id="26600-106">S2</span></span>
```
Start-AzWebAppSlot [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="26600-107">描述</span><span class="sxs-lookup"><span data-stu-id="26600-107">DESCRIPTION</span></span>
<span data-ttu-id="26600-108">**Start-AzWebAppSlot** Cmdlet 會啟動 Azure Web App Slot。</span><span class="sxs-lookup"><span data-stu-id="26600-108">The **Start-AzWebAppSlot** cmdlet starts an Azure Web App Slot.</span></span>

## <span data-ttu-id="26600-109">例子</span><span class="sxs-lookup"><span data-stu-id="26600-109">EXAMPLES</span></span>

### <span data-ttu-id="26600-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="26600-110">Example 1</span></span>
```
PS C:\>Start-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="26600-111">此命令會啟動名為 Slot001 的 Slot，與名稱為 ContosoWebApp 的 Web App 相關，該 Web App 屬於 Default-Web-WestUS 資源群組。</span><span class="sxs-lookup"><span data-stu-id="26600-111">This command starts the Slot named Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="26600-112">參數</span><span class="sxs-lookup"><span data-stu-id="26600-112">PARAMETERS</span></span>

### <span data-ttu-id="26600-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26600-113">-DefaultProfile</span></span>
<span data-ttu-id="26600-114">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="26600-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="26600-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="26600-115">-Name</span></span>
<span data-ttu-id="26600-116">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="26600-116">WebApp Name</span></span>

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

### <span data-ttu-id="26600-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26600-117">-ResourceGroupName</span></span>
<span data-ttu-id="26600-118">資源組名</span><span class="sxs-lookup"><span data-stu-id="26600-118">Resource Group Name</span></span>

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

### <span data-ttu-id="26600-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="26600-119">-Slot</span></span>
<span data-ttu-id="26600-120">WebApp Slot 名稱</span><span class="sxs-lookup"><span data-stu-id="26600-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="26600-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="26600-121">-WebApp</span></span>
<span data-ttu-id="26600-122">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="26600-122">WebApp Object</span></span>

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

### <span data-ttu-id="26600-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26600-123">CommonParameters</span></span>
<span data-ttu-id="26600-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="26600-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26600-125">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="26600-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26600-126">輸入</span><span class="sxs-lookup"><span data-stu-id="26600-126">INPUTS</span></span>

### <span data-ttu-id="26600-127">System.String</span><span class="sxs-lookup"><span data-stu-id="26600-127">System.String</span></span>

### <span data-ttu-id="26600-128">Microsoft.Azure.Commands.WebApps.models.PSSite</span><span class="sxs-lookup"><span data-stu-id="26600-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="26600-129">輸出</span><span class="sxs-lookup"><span data-stu-id="26600-129">OUTPUTS</span></span>

### <span data-ttu-id="26600-130">Microsoft.Azure.Commands.WebApps.models.PSSite</span><span class="sxs-lookup"><span data-stu-id="26600-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="26600-131">筆記</span><span class="sxs-lookup"><span data-stu-id="26600-131">NOTES</span></span>

## <span data-ttu-id="26600-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="26600-132">RELATED LINKS</span></span>

[<span data-ttu-id="26600-133">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="26600-133">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="26600-134">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="26600-134">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="26600-135">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="26600-135">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="26600-136">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="26600-136">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="26600-137">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="26600-137">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="26600-138">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="26600-138">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="26600-139">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="26600-139">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
