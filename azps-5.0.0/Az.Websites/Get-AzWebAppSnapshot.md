---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSnapshot.md
ms.openlocfilehash: 350f7d5b44f5a1c84f97511a4febb7d967ee2de4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138570"
---
# <span data-ttu-id="55485-101">Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="55485-101">Get-AzWebAppSnapshot</span></span>

## <span data-ttu-id="55485-102">摘要</span><span class="sxs-lookup"><span data-stu-id="55485-102">SYNOPSIS</span></span>
<span data-ttu-id="55485-103">取得適用于 web 應用程式的快照。</span><span class="sxs-lookup"><span data-stu-id="55485-103">Gets the snapshots available for a web app.</span></span>

## <span data-ttu-id="55485-104">句法</span><span class="sxs-lookup"><span data-stu-id="55485-104">SYNTAX</span></span>

### <span data-ttu-id="55485-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="55485-105">FromResourceName</span></span>
```
Get-AzWebAppSnapshot [-UseDisasterRecovery] [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="55485-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="55485-106">FromWebApp</span></span>
```
Get-AzWebAppSnapshot [-UseDisasterRecovery] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="55485-107">說明</span><span class="sxs-lookup"><span data-stu-id="55485-107">DESCRIPTION</span></span>
<span data-ttu-id="55485-108">**AzWebAppSnapshot** Cmdlet 會傳回 web 應用程式的所有快照。</span><span class="sxs-lookup"><span data-stu-id="55485-108">The **Get-AzWebAppSnapshot** cmdlet returns all snapshots for a web app.</span></span> <span data-ttu-id="55485-109">快照是 web 應用程式檔案和設定的自動備份。</span><span class="sxs-lookup"><span data-stu-id="55485-109">Snapshots are automatic backups of a web app's files and settings.</span></span> <span data-ttu-id="55485-110">您可以使用 **Restore AzWebAppSnapshot** Cmdlet 來還原快照。</span><span class="sxs-lookup"><span data-stu-id="55485-110">A snapshot can be restored with the **Restore-AzWebAppSnapshot** cmdlet.</span></span>

## <span data-ttu-id="55485-111">示例</span><span class="sxs-lookup"><span data-stu-id="55485-111">EXAMPLES</span></span>

### <span data-ttu-id="55485-112">範例1</span><span class="sxs-lookup"><span data-stu-id="55485-112">Example 1</span></span>
```
PS C:\> Get-AzWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Staging"
```

<span data-ttu-id="55485-113">取得名為「ContosoApp」的 web app 快照，並在「預設-Web-WestUS」資源群組中使用名為「暫存」的槽</span><span class="sxs-lookup"><span data-stu-id="55485-113">Get the snapshots for a web app named "ContosoApp" with a slot named "Staging" in the "Default-Web-WestUS" resource group</span></span>

## <span data-ttu-id="55485-114">參數</span><span class="sxs-lookup"><span data-stu-id="55485-114">PARAMETERS</span></span>

### <span data-ttu-id="55485-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55485-115">-DefaultProfile</span></span>
<span data-ttu-id="55485-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="55485-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55485-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="55485-117">-Name</span></span>
<span data-ttu-id="55485-118">Web 應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="55485-118">The name of the web app.</span></span>

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

### <span data-ttu-id="55485-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55485-119">-ResourceGroupName</span></span>
<span data-ttu-id="55485-120">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="55485-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="55485-121">-槽</span><span class="sxs-lookup"><span data-stu-id="55485-121">-Slot</span></span>
<span data-ttu-id="55485-122">Web 應用程式槽的名稱。</span><span class="sxs-lookup"><span data-stu-id="55485-122">The name of the web app slot.</span></span>

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

### <span data-ttu-id="55485-123">-UseDisasterRecovery</span><span class="sxs-lookup"><span data-stu-id="55485-123">-UseDisasterRecovery</span></span>
<span data-ttu-id="55485-124">從副刻度單元讀取快照。</span><span class="sxs-lookup"><span data-stu-id="55485-124">Read the snapshots from a secondary scale unit.</span></span>

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

### <span data-ttu-id="55485-125">-WebApp</span><span class="sxs-lookup"><span data-stu-id="55485-125">-WebApp</span></span>
<span data-ttu-id="55485-126">Web app 物件</span><span class="sxs-lookup"><span data-stu-id="55485-126">The web app object</span></span>

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

### <span data-ttu-id="55485-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55485-127">CommonParameters</span></span>
<span data-ttu-id="55485-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="55485-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55485-129">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="55485-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55485-130">輸入</span><span class="sxs-lookup"><span data-stu-id="55485-130">INPUTS</span></span>

### <span data-ttu-id="55485-131">System.object</span><span class="sxs-lookup"><span data-stu-id="55485-131">System.String</span></span>

### <span data-ttu-id="55485-132">PSSite 中的 WebApps。</span><span class="sxs-lookup"><span data-stu-id="55485-132">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="55485-133">輸出</span><span class="sxs-lookup"><span data-stu-id="55485-133">OUTPUTS</span></span>

### <span data-ttu-id="55485-134">WebApps BackupRestore. AzureWebAppSnapshot （）</span><span class="sxs-lookup"><span data-stu-id="55485-134">Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot</span></span>

## <span data-ttu-id="55485-135">筆記</span><span class="sxs-lookup"><span data-stu-id="55485-135">NOTES</span></span>

## <span data-ttu-id="55485-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="55485-136">RELATED LINKS</span></span>
