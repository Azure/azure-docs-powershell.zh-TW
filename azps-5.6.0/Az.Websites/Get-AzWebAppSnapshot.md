---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/get-azwebappsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSnapshot.md
ms.openlocfilehash: 14567157501b81ba669061285025ba1631be88d4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908693"
---
# <span data-ttu-id="fcd5a-101">Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="fcd5a-101">Get-AzWebAppSnapshot</span></span>

## <span data-ttu-id="fcd5a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="fcd5a-102">SYNOPSIS</span></span>
<span data-ttu-id="fcd5a-103">為 Web 應用程式提供快照。</span><span class="sxs-lookup"><span data-stu-id="fcd5a-103">Gets the snapshots available for a web app.</span></span>

## <span data-ttu-id="fcd5a-104">語法</span><span class="sxs-lookup"><span data-stu-id="fcd5a-104">SYNTAX</span></span>

### <span data-ttu-id="fcd5a-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="fcd5a-105">FromResourceName</span></span>
```
Get-AzWebAppSnapshot [-UseDisasterRecovery] [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fcd5a-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="fcd5a-106">FromWebApp</span></span>
```
Get-AzWebAppSnapshot [-UseDisasterRecovery] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fcd5a-107">描述</span><span class="sxs-lookup"><span data-stu-id="fcd5a-107">DESCRIPTION</span></span>
<span data-ttu-id="fcd5a-108">**Get-AzWebAppSnapshot** Cmdlet 會返回 Web 應用程式的所有快照。</span><span class="sxs-lookup"><span data-stu-id="fcd5a-108">The **Get-AzWebAppSnapshot** cmdlet returns all snapshots for a web app.</span></span> <span data-ttu-id="fcd5a-109">快照是 Web App 檔案和設定自動備份。</span><span class="sxs-lookup"><span data-stu-id="fcd5a-109">Snapshots are automatic backups of a web app's files and settings.</span></span> <span data-ttu-id="fcd5a-110">您可以使用 **Restore-AzWebAppSnapshot Cmdlet** 還原快照。</span><span class="sxs-lookup"><span data-stu-id="fcd5a-110">A snapshot can be restored with the **Restore-AzWebAppSnapshot** cmdlet.</span></span>

## <span data-ttu-id="fcd5a-111">例子</span><span class="sxs-lookup"><span data-stu-id="fcd5a-111">EXAMPLES</span></span>

### <span data-ttu-id="fcd5a-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="fcd5a-112">Example 1</span></span>
```
PS C:\> Get-AzWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Staging"
```

<span data-ttu-id="fcd5a-113">取得名為 「ContosoApp」的 Web App 的快照，以及 "Default-Web-WestUS" 資源群組中名為「暫存」的時段</span><span class="sxs-lookup"><span data-stu-id="fcd5a-113">Get the snapshots for a web app named "ContosoApp" with a slot named "Staging" in the "Default-Web-WestUS" resource group</span></span>

## <span data-ttu-id="fcd5a-114">參數</span><span class="sxs-lookup"><span data-stu-id="fcd5a-114">PARAMETERS</span></span>

### <span data-ttu-id="fcd5a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcd5a-115">-DefaultProfile</span></span>
<span data-ttu-id="fcd5a-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="fcd5a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fcd5a-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="fcd5a-117">-Name</span></span>
<span data-ttu-id="fcd5a-118">Web 應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="fcd5a-118">The name of the web app.</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fcd5a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fcd5a-119">-ResourceGroupName</span></span>
<span data-ttu-id="fcd5a-120">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="fcd5a-120">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fcd5a-121">-Slot</span><span class="sxs-lookup"><span data-stu-id="fcd5a-121">-Slot</span></span>
<span data-ttu-id="fcd5a-122">Web App 插槽的名稱。</span><span class="sxs-lookup"><span data-stu-id="fcd5a-122">The name of the web app slot.</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fcd5a-123">-UseD區sterRecovery</span><span class="sxs-lookup"><span data-stu-id="fcd5a-123">-UseDisasterRecovery</span></span>
<span data-ttu-id="fcd5a-124">讀取次要縮放單位的快照。</span><span class="sxs-lookup"><span data-stu-id="fcd5a-124">Read the snapshots from a secondary scale unit.</span></span>

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

### <span data-ttu-id="fcd5a-125">-WebApp</span><span class="sxs-lookup"><span data-stu-id="fcd5a-125">-WebApp</span></span>
<span data-ttu-id="fcd5a-126">Web App 物件</span><span class="sxs-lookup"><span data-stu-id="fcd5a-126">The web app object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: FromWebApp
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fcd5a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcd5a-127">CommonParameters</span></span>
<span data-ttu-id="fcd5a-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="fcd5a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcd5a-129">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="fcd5a-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcd5a-130">輸入</span><span class="sxs-lookup"><span data-stu-id="fcd5a-130">INPUTS</span></span>

### <span data-ttu-id="fcd5a-131">System.String</span><span class="sxs-lookup"><span data-stu-id="fcd5a-131">System.String</span></span>

### <span data-ttu-id="fcd5a-132">Microsoft.Azure.Commands.WebApps.models.PSSite</span><span class="sxs-lookup"><span data-stu-id="fcd5a-132">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="fcd5a-133">輸出</span><span class="sxs-lookup"><span data-stu-id="fcd5a-133">OUTPUTS</span></span>

### <span data-ttu-id="fcd5a-134">Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="fcd5a-134">Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot</span></span>

## <span data-ttu-id="fcd5a-135">筆記</span><span class="sxs-lookup"><span data-stu-id="fcd5a-135">NOTES</span></span>

## <span data-ttu-id="fcd5a-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="fcd5a-136">RELATED LINKS</span></span>
