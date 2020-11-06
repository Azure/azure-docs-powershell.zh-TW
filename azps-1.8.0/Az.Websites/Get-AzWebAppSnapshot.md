---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSnapshot.md
ms.openlocfilehash: fab46f997492c366857c7d13bea38543cca4e91c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93614285"
---
# <span data-ttu-id="1569f-101">Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="1569f-101">Get-AzWebAppSnapshot</span></span>

## <span data-ttu-id="1569f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1569f-102">SYNOPSIS</span></span>
<span data-ttu-id="1569f-103">取得適用于 web 應用程式的快照。</span><span class="sxs-lookup"><span data-stu-id="1569f-103">Gets the snapshots available for a web app.</span></span>

## <span data-ttu-id="1569f-104">句法</span><span class="sxs-lookup"><span data-stu-id="1569f-104">SYNTAX</span></span>

### <span data-ttu-id="1569f-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="1569f-105">FromResourceName</span></span>
```
Get-AzWebAppSnapshot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1569f-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="1569f-106">FromWebApp</span></span>
```
Get-AzWebAppSnapshot [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1569f-107">說明</span><span class="sxs-lookup"><span data-stu-id="1569f-107">DESCRIPTION</span></span>
<span data-ttu-id="1569f-108">**AzWebAppSnapshot** Cmdlet 會傳回 web 應用程式的所有快照。</span><span class="sxs-lookup"><span data-stu-id="1569f-108">The **Get-AzWebAppSnapshot** cmdlet returns all snapshots for a web app.</span></span> <span data-ttu-id="1569f-109">快照是 web 應用程式檔案和設定的自動備份。</span><span class="sxs-lookup"><span data-stu-id="1569f-109">Snapshots are automatic backups of a web app's files and settings.</span></span> <span data-ttu-id="1569f-110">您可以使用 **Restore AzWebAppSnapshot** Cmdlet 來還原快照。</span><span class="sxs-lookup"><span data-stu-id="1569f-110">A snapshot can be restored with the **Restore-AzWebAppSnapshot** cmdlet.</span></span>

## <span data-ttu-id="1569f-111">示例</span><span class="sxs-lookup"><span data-stu-id="1569f-111">EXAMPLES</span></span>

### <span data-ttu-id="1569f-112">範例1</span><span class="sxs-lookup"><span data-stu-id="1569f-112">Example 1</span></span>
```
PS C:\> Get-AzWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Staging"
```

<span data-ttu-id="1569f-113">取得名為「ConstosoApp」的 web app 快照，並在「預設-Web-WestUS」資源群組中使用名為「暫存」的槽</span><span class="sxs-lookup"><span data-stu-id="1569f-113">Get the snapshots for a web app named "ConstosoApp" with a slot named "Staging" in the "Default-Web-WestUS" resource group</span></span>

## <span data-ttu-id="1569f-114">參數</span><span class="sxs-lookup"><span data-stu-id="1569f-114">PARAMETERS</span></span>

### <span data-ttu-id="1569f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1569f-115">-DefaultProfile</span></span>
<span data-ttu-id="1569f-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1569f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1569f-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="1569f-117">-Name</span></span>
<span data-ttu-id="1569f-118">Web 應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="1569f-118">The name of the web app.</span></span>

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

### <span data-ttu-id="1569f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1569f-119">-ResourceGroupName</span></span>
<span data-ttu-id="1569f-120">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1569f-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="1569f-121">-槽</span><span class="sxs-lookup"><span data-stu-id="1569f-121">-Slot</span></span>
<span data-ttu-id="1569f-122">Web 應用程式槽的名稱。</span><span class="sxs-lookup"><span data-stu-id="1569f-122">The name of the web app slot.</span></span>

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

### <span data-ttu-id="1569f-123">-WebApp</span><span class="sxs-lookup"><span data-stu-id="1569f-123">-WebApp</span></span>
<span data-ttu-id="1569f-124">Web app 物件</span><span class="sxs-lookup"><span data-stu-id="1569f-124">The web app object</span></span>

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

### <span data-ttu-id="1569f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1569f-125">CommonParameters</span></span>
<span data-ttu-id="1569f-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1569f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1569f-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1569f-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1569f-128">輸入</span><span class="sxs-lookup"><span data-stu-id="1569f-128">INPUTS</span></span>

### <span data-ttu-id="1569f-129">System.object</span><span class="sxs-lookup"><span data-stu-id="1569f-129">System.String</span></span>

### <span data-ttu-id="1569f-130">PSSite 中的 WebApps。</span><span class="sxs-lookup"><span data-stu-id="1569f-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="1569f-131">輸出</span><span class="sxs-lookup"><span data-stu-id="1569f-131">OUTPUTS</span></span>

### <span data-ttu-id="1569f-132">WebApps BackupRestore. AzureWebAppSnapshot （）</span><span class="sxs-lookup"><span data-stu-id="1569f-132">Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot</span></span>

## <span data-ttu-id="1569f-133">筆記</span><span class="sxs-lookup"><span data-stu-id="1569f-133">NOTES</span></span>

## <span data-ttu-id="1569f-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="1569f-134">RELATED LINKS</span></span>
