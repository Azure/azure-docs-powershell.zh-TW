---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 9057185C-6F22-4C4A-8480-BE542B5D6BAF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/remove-azurermwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebApp.md
ms.openlocfilehash: a984a9a76a41db93bee96acfa029ca05a30d85f0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447562"
---
# <span data-ttu-id="3a8fb-101">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="3a8fb-101">Remove-AzureRmWebApp</span></span>

## <span data-ttu-id="3a8fb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3a8fb-102">SYNOPSIS</span></span>
<span data-ttu-id="3a8fb-103">移除 Azure Web App。</span><span class="sxs-lookup"><span data-stu-id="3a8fb-103">Removes an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3a8fb-104">句法</span><span class="sxs-lookup"><span data-stu-id="3a8fb-104">SYNTAX</span></span>

### <span data-ttu-id="3a8fb-105">S1</span><span class="sxs-lookup"><span data-stu-id="3a8fb-105">S1</span></span>
```
Remove-AzureRmWebApp [-Force] [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a8fb-106">S2</span><span class="sxs-lookup"><span data-stu-id="3a8fb-106">S2</span></span>
```
Remove-AzureRmWebApp [-Force] [-WebApp] <Site> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3a8fb-107">說明</span><span class="sxs-lookup"><span data-stu-id="3a8fb-107">DESCRIPTION</span></span>
<span data-ttu-id="3a8fb-108">**AzureRmWebApp** Cmdlet 會移除 Azure Web App 提供的資源群組和 Web app 名稱。</span><span class="sxs-lookup"><span data-stu-id="3a8fb-108">The **Remove-AzureRmWebApp** cmdlet removes an Azure Web App provided the resource group and Web App name.</span></span>
<span data-ttu-id="3a8fb-109">這個 Cmdlet 預設會同時移除所有的槽與躍點數。</span><span class="sxs-lookup"><span data-stu-id="3a8fb-109">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="3a8fb-110">示例</span><span class="sxs-lookup"><span data-stu-id="3a8fb-110">EXAMPLES</span></span>

### <span data-ttu-id="3a8fb-111">範例1：移除 Web 應用程式</span><span class="sxs-lookup"><span data-stu-id="3a8fb-111">Example 1: Remove a Web App</span></span>
```
PS C:\>Remove-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="3a8fb-112">這個命令會移除名為 ContosoSite 的 Azure Web App，該應用程式屬於名為「預設-Web-WestUS」的資源群組。</span><span class="sxs-lookup"><span data-stu-id="3a8fb-112">This command removes the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="3a8fb-113">參數</span><span class="sxs-lookup"><span data-stu-id="3a8fb-113">PARAMETERS</span></span>

### <span data-ttu-id="3a8fb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a8fb-114">-DefaultProfile</span></span>
<span data-ttu-id="3a8fb-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3a8fb-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a8fb-116">-Force</span><span class="sxs-lookup"><span data-stu-id="3a8fb-116">-Force</span></span>
<span data-ttu-id="3a8fb-117">[強制移除] 選項</span><span class="sxs-lookup"><span data-stu-id="3a8fb-117">Forcefully Remove Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a8fb-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="3a8fb-118">-Name</span></span>
<span data-ttu-id="3a8fb-119">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="3a8fb-119">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a8fb-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a8fb-120">-ResourceGroupName</span></span>
<span data-ttu-id="3a8fb-121">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="3a8fb-121">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a8fb-122">-WebApp</span><span class="sxs-lookup"><span data-stu-id="3a8fb-122">-WebApp</span></span>
<span data-ttu-id="3a8fb-123">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="3a8fb-123">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3a8fb-124">-確認</span><span class="sxs-lookup"><span data-stu-id="3a8fb-124">-Confirm</span></span>
<span data-ttu-id="3a8fb-125">在執行 Cmdlet 之前提示您進行確認。在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3a8fb-125">Prompts you for confirmation before running the cmdlet.Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a8fb-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a8fb-126">-WhatIf</span></span>
<span data-ttu-id="3a8fb-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3a8fb-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a8fb-128">未執行 Cmdlet。顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3a8fb-128">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a8fb-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3a8fb-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a8fb-130">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3a8fb-130">-AsJob</span></span>
<span data-ttu-id="3a8fb-131">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="3a8fb-131">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a8fb-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a8fb-132">CommonParameters</span></span>
<span data-ttu-id="3a8fb-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3a8fb-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a8fb-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3a8fb-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a8fb-135">輸入</span><span class="sxs-lookup"><span data-stu-id="3a8fb-135">INPUTS</span></span>

### <span data-ttu-id="3a8fb-136">網站地圖</span><span class="sxs-lookup"><span data-stu-id="3a8fb-136">Site</span></span>
<span data-ttu-id="3a8fb-137">形參 "WebApp" 接受管線中 "Site" 類型的值</span><span class="sxs-lookup"><span data-stu-id="3a8fb-137">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="3a8fb-138">輸出</span><span class="sxs-lookup"><span data-stu-id="3a8fb-138">OUTPUTS</span></span>

## <span data-ttu-id="3a8fb-139">筆記</span><span class="sxs-lookup"><span data-stu-id="3a8fb-139">NOTES</span></span>

## <span data-ttu-id="3a8fb-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="3a8fb-140">RELATED LINKS</span></span>

[<span data-ttu-id="3a8fb-141">AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="3a8fb-141">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="3a8fb-142">新-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="3a8fb-142">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="3a8fb-143">重新開機-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="3a8fb-143">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="3a8fb-144">開始-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="3a8fb-144">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="3a8fb-145">停止 AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="3a8fb-145">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


