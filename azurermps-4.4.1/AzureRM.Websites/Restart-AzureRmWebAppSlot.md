---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 645E74D2-640D-494F-9798-4375FE6A0AF2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restart-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restart-AzureRmWebAppSlot.md
ms.openlocfilehash: ace1b16bc6d89fb619daba23a214326acd8d0d24
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444868"
---
# <span data-ttu-id="54821-101">Restart-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="54821-101">Restart-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="54821-102">摘要</span><span class="sxs-lookup"><span data-stu-id="54821-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="54821-103">句法</span><span class="sxs-lookup"><span data-stu-id="54821-103">SYNTAX</span></span>

### <span data-ttu-id="54821-104">S1</span><span class="sxs-lookup"><span data-stu-id="54821-104">S1</span></span>
```
Restart-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="54821-105">S2</span><span class="sxs-lookup"><span data-stu-id="54821-105">S2</span></span>
```
Restart-AzureRmWebAppSlot [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="54821-106">說明</span><span class="sxs-lookup"><span data-stu-id="54821-106">DESCRIPTION</span></span>
<span data-ttu-id="54821-107">**Restart AzureRmWebAppSlot** Cmdlet 會停止，然後啟動 Azure Web App 槽。</span><span class="sxs-lookup"><span data-stu-id="54821-107">The **Restart-AzureRmWebAppSlot** cmdlet stops and then starts an Azure Web App Slot.</span></span>
<span data-ttu-id="54821-108">如果 Web 應用程式槽處於停止狀態，請使用 Start-AzureRmWebAppSlot Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="54821-108">If the Web App Slot is in a stopped state, use the Start-AzureRmWebAppSlot cmdlet.</span></span>

## <span data-ttu-id="54821-109">示例</span><span class="sxs-lookup"><span data-stu-id="54821-109">EXAMPLES</span></span>

### <span data-ttu-id="54821-110">範例1</span><span class="sxs-lookup"><span data-stu-id="54821-110">Example 1</span></span>
```
PS C:\> Restart-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="54821-111">這個命令會重新開機與資源群組 Slot001 相關聯之 web app ContosoWebApp 的槽，其預設為 Web-WestUS</span><span class="sxs-lookup"><span data-stu-id="54821-111">This command restarts the slot Slot001 for the web app ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="54821-112">參數</span><span class="sxs-lookup"><span data-stu-id="54821-112">PARAMETERS</span></span>

### <span data-ttu-id="54821-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="54821-113">-Name</span></span>
<span data-ttu-id="54821-114">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="54821-114">WebApp Name</span></span>

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

### <span data-ttu-id="54821-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54821-115">-ResourceGroupName</span></span>
<span data-ttu-id="54821-116">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="54821-116">Resource Group Name</span></span>

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

### <span data-ttu-id="54821-117">-槽</span><span class="sxs-lookup"><span data-stu-id="54821-117">-Slot</span></span>
<span data-ttu-id="54821-118">WebApp 槽名稱</span><span class="sxs-lookup"><span data-stu-id="54821-118">WebApp Slot Name</span></span>

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

### <span data-ttu-id="54821-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="54821-119">-WebApp</span></span>
<span data-ttu-id="54821-120">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="54821-120">WebApp Object</span></span>

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

### <span data-ttu-id="54821-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54821-121">-DefaultProfile</span></span>
<span data-ttu-id="54821-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="54821-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54821-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54821-123">CommonParameters</span></span>
<span data-ttu-id="54821-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="54821-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54821-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="54821-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54821-126">輸入</span><span class="sxs-lookup"><span data-stu-id="54821-126">INPUTS</span></span>

### <span data-ttu-id="54821-127">網站地圖</span><span class="sxs-lookup"><span data-stu-id="54821-127">Site</span></span>
<span data-ttu-id="54821-128">形參 "WebApp" 接受管線中 "Site" 類型的值</span><span class="sxs-lookup"><span data-stu-id="54821-128">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="54821-129">輸出</span><span class="sxs-lookup"><span data-stu-id="54821-129">OUTPUTS</span></span>

## <span data-ttu-id="54821-130">筆記</span><span class="sxs-lookup"><span data-stu-id="54821-130">NOTES</span></span>

## <span data-ttu-id="54821-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="54821-131">RELATED LINKS</span></span>

[<span data-ttu-id="54821-132">AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="54821-132">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="54821-133">新-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="54821-133">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="54821-134">移除-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="54821-134">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="54821-135">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="54821-135">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="54821-136">開始-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="54821-136">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="54821-137">停止 AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="54821-137">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="54821-138">AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="54821-138">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
