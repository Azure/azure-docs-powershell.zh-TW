---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 0FDDDEE1-CEAD-46DA-A7EB-EE477ED59749
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/start-azurermwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Start-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Start-AzureRmWebAppSlot.md
ms.openlocfilehash: 089711bacd6401b4c44683a159e43a92a56106d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445295"
---
# <span data-ttu-id="33898-101">Start-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="33898-101">Start-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="33898-102">摘要</span><span class="sxs-lookup"><span data-stu-id="33898-102">SYNOPSIS</span></span>
<span data-ttu-id="33898-103">啟動 Azure Web App 槽。</span><span class="sxs-lookup"><span data-stu-id="33898-103">Starts an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="33898-104">句法</span><span class="sxs-lookup"><span data-stu-id="33898-104">SYNTAX</span></span>

### <span data-ttu-id="33898-105">S1</span><span class="sxs-lookup"><span data-stu-id="33898-105">S1</span></span>
```
Start-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="33898-106">S2</span><span class="sxs-lookup"><span data-stu-id="33898-106">S2</span></span>
```
Start-AzureRmWebAppSlot [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="33898-107">說明</span><span class="sxs-lookup"><span data-stu-id="33898-107">DESCRIPTION</span></span>
<span data-ttu-id="33898-108">**AzureRmWebAppSlot** Cmdlet 會啟動 Azure Web App 槽。</span><span class="sxs-lookup"><span data-stu-id="33898-108">The **Start-AzureRmWebAppSlot** cmdlet starts an Azure Web App Slot.</span></span>

## <span data-ttu-id="33898-109">示例</span><span class="sxs-lookup"><span data-stu-id="33898-109">EXAMPLES</span></span>

### <span data-ttu-id="33898-110">範例1</span><span class="sxs-lookup"><span data-stu-id="33898-110">Example 1</span></span>
```
PS C:\>Start-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="33898-111">這個命令會啟動一個名為 Slot001 的槽，該槽屬於名為 [Default-Web-WestUS] 的資源群組的名為 ContosoWebApp 的 Web App。</span><span class="sxs-lookup"><span data-stu-id="33898-111">This command starts the Slot named Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="33898-112">參數</span><span class="sxs-lookup"><span data-stu-id="33898-112">PARAMETERS</span></span>

### <span data-ttu-id="33898-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33898-113">-DefaultProfile</span></span>
<span data-ttu-id="33898-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="33898-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="33898-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="33898-115">-Name</span></span>
<span data-ttu-id="33898-116">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="33898-116">WebApp Name</span></span>

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

### <span data-ttu-id="33898-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33898-117">-ResourceGroupName</span></span>
<span data-ttu-id="33898-118">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="33898-118">Resource Group Name</span></span>

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

### <span data-ttu-id="33898-119">-槽</span><span class="sxs-lookup"><span data-stu-id="33898-119">-Slot</span></span>
<span data-ttu-id="33898-120">WebApp 槽名稱</span><span class="sxs-lookup"><span data-stu-id="33898-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="33898-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="33898-121">-WebApp</span></span>
<span data-ttu-id="33898-122">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="33898-122">WebApp Object</span></span>

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

### <span data-ttu-id="33898-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33898-123">CommonParameters</span></span>
<span data-ttu-id="33898-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="33898-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33898-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="33898-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33898-126">輸入</span><span class="sxs-lookup"><span data-stu-id="33898-126">INPUTS</span></span>

### <span data-ttu-id="33898-127">System.object</span><span class="sxs-lookup"><span data-stu-id="33898-127">System.String</span></span>

### <span data-ttu-id="33898-128">[Microsoft Azure. 管理] 網站</span><span class="sxs-lookup"><span data-stu-id="33898-128">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="33898-129">參數： WebApp (ByValue) </span><span class="sxs-lookup"><span data-stu-id="33898-129">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="33898-130">輸出</span><span class="sxs-lookup"><span data-stu-id="33898-130">OUTPUTS</span></span>

### <span data-ttu-id="33898-131">[Microsoft Azure. 管理] 網站</span><span class="sxs-lookup"><span data-stu-id="33898-131">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="33898-132">筆記</span><span class="sxs-lookup"><span data-stu-id="33898-132">NOTES</span></span>

## <span data-ttu-id="33898-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="33898-133">RELATED LINKS</span></span>

[<span data-ttu-id="33898-134">AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="33898-134">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="33898-135">新-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="33898-135">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="33898-136">移除-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="33898-136">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="33898-137">重新開機-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="33898-137">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="33898-138">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="33898-138">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="33898-139">停止 AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="33898-139">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="33898-140">AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="33898-140">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
