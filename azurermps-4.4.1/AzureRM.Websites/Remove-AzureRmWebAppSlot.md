---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppSlot.md
ms.openlocfilehash: 65393bc3dd2e9e6b51699a21baf0e6d3750464bf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456311"
---
# <span data-ttu-id="5417e-101">Remove-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="5417e-101">Remove-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="5417e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5417e-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5417e-103">句法</span><span class="sxs-lookup"><span data-stu-id="5417e-103">SYNTAX</span></span>

### <span data-ttu-id="5417e-104">S1</span><span class="sxs-lookup"><span data-stu-id="5417e-104">S1</span></span>
```
Remove-AzureRmWebAppSlot [-Force] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5417e-105">S2</span><span class="sxs-lookup"><span data-stu-id="5417e-105">S2</span></span>
```
Remove-AzureRmWebAppSlot [-Force] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5417e-106">說明</span><span class="sxs-lookup"><span data-stu-id="5417e-106">DESCRIPTION</span></span>
<span data-ttu-id="5417e-107">**AzureRmWebAppSlot** Cmdlet 會移除 Azure Web App 槽，前提是資源群組和 Web 應用程式名稱。</span><span class="sxs-lookup"><span data-stu-id="5417e-107">The **Remove-AzureRmWebAppSlot** cmdlet removes an Azure Web App Slot provided the resource group and Web App name.</span></span>
<span data-ttu-id="5417e-108">這個 Cmdlet 預設會同時移除所有的槽與躍點數。</span><span class="sxs-lookup"><span data-stu-id="5417e-108">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="5417e-109">示例</span><span class="sxs-lookup"><span data-stu-id="5417e-109">EXAMPLES</span></span>

### <span data-ttu-id="5417e-110">範例1：移除 Web 應用程式槽</span><span class="sxs-lookup"><span data-stu-id="5417e-110">Example 1: Remove a Web App Slot</span></span>
```
PS C:\>Remove-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="5417e-111">這個命令會移除與屬於名為 Default-Web WestUS 之資源群組的 Web App ContosoSite 相關聯的槽 Slot001。</span><span class="sxs-lookup"><span data-stu-id="5417e-111">This command removes the Slot named Slot001 associated with Web App ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="5417e-112">參數</span><span class="sxs-lookup"><span data-stu-id="5417e-112">PARAMETERS</span></span>

### <span data-ttu-id="5417e-113">-Force</span><span class="sxs-lookup"><span data-stu-id="5417e-113">-Force</span></span>
<span data-ttu-id="5417e-114">[強制移除] 選項</span><span class="sxs-lookup"><span data-stu-id="5417e-114">Forcefully Remove Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5417e-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="5417e-115">-Name</span></span>
<span data-ttu-id="5417e-116">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="5417e-116">WebApp Name</span></span>

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

### <span data-ttu-id="5417e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5417e-117">-ResourceGroupName</span></span>
<span data-ttu-id="5417e-118">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="5417e-118">Resource Group Name</span></span>

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

### <span data-ttu-id="5417e-119">-槽</span><span class="sxs-lookup"><span data-stu-id="5417e-119">-Slot</span></span>
<span data-ttu-id="5417e-120">WebApp 槽名稱</span><span class="sxs-lookup"><span data-stu-id="5417e-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="5417e-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="5417e-121">-WebApp</span></span>
<span data-ttu-id="5417e-122">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="5417e-122">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5417e-123">-確認</span><span class="sxs-lookup"><span data-stu-id="5417e-123">-Confirm</span></span>
<span data-ttu-id="5417e-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5417e-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5417e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5417e-125">-WhatIf</span></span>
<span data-ttu-id="5417e-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5417e-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5417e-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5417e-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5417e-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5417e-128">-DefaultProfile</span></span>
<span data-ttu-id="5417e-129">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5417e-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5417e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5417e-130">CommonParameters</span></span>
<span data-ttu-id="5417e-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5417e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5417e-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5417e-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5417e-133">輸入</span><span class="sxs-lookup"><span data-stu-id="5417e-133">INPUTS</span></span>

### <span data-ttu-id="5417e-134">網站地圖</span><span class="sxs-lookup"><span data-stu-id="5417e-134">Site</span></span>
<span data-ttu-id="5417e-135">形參 "WebApp" 接受管線中 "Site" 類型的值</span><span class="sxs-lookup"><span data-stu-id="5417e-135">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="5417e-136">輸出</span><span class="sxs-lookup"><span data-stu-id="5417e-136">OUTPUTS</span></span>

### <span data-ttu-id="5417e-137">AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="5417e-137">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="5417e-138">筆記</span><span class="sxs-lookup"><span data-stu-id="5417e-138">NOTES</span></span>

## <span data-ttu-id="5417e-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="5417e-139">RELATED LINKS</span></span>

[<span data-ttu-id="5417e-140">AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="5417e-140">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="5417e-141">新-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="5417e-141">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="5417e-142">重新開機-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="5417e-142">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="5417e-143">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="5417e-143">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="5417e-144">開始-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="5417e-144">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="5417e-145">停止 AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="5417e-145">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="5417e-146">AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="5417e-146">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
