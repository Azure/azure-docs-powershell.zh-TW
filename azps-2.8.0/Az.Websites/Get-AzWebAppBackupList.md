---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: BBC85035-DCF7-44FA-A747-A1563A55B820
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappbackuplist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackupList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackupList.md
ms.openlocfilehash: fab8973c63e419cdef45fb79a0ad5182c46f2de5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93793283"
---
# <span data-ttu-id="4120b-101">Get-AzWebAppBackupList</span><span class="sxs-lookup"><span data-stu-id="4120b-101">Get-AzWebAppBackupList</span></span>

## <span data-ttu-id="4120b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4120b-102">SYNOPSIS</span></span>

## <span data-ttu-id="4120b-103">句法</span><span class="sxs-lookup"><span data-stu-id="4120b-103">SYNTAX</span></span>

### <span data-ttu-id="4120b-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="4120b-104">FromResourceName</span></span>
```
Get-AzWebAppBackupList [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4120b-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="4120b-105">FromWebApp</span></span>
```
Get-AzWebAppBackupList [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4120b-106">說明</span><span class="sxs-lookup"><span data-stu-id="4120b-106">DESCRIPTION</span></span>
<span data-ttu-id="4120b-107">**AzWebAppBackupList** Cmdlet 會取得 Azure Web App 備份的清單。</span><span class="sxs-lookup"><span data-stu-id="4120b-107">The **Get-AzWebAppBackupList** cmdlet gets a list of backups for an Azure Web App.</span></span>

## <span data-ttu-id="4120b-108">示例</span><span class="sxs-lookup"><span data-stu-id="4120b-108">EXAMPLES</span></span>

### <span data-ttu-id="4120b-109">sr-1</span><span class="sxs-lookup"><span data-stu-id="4120b-109">1:</span></span>
```
PS C:\>Get-AzWebAppBackupList -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="4120b-110">這個命令會傳回與資源群組 ContosoResourceGroup 相關聯之 WebApp WebAppStandard 的備份清單。</span><span class="sxs-lookup"><span data-stu-id="4120b-110">This command returns a backup list pertaining to WebApp WebAppStandard associated with the resource group ContosoResourceGroup.</span></span>

## <span data-ttu-id="4120b-111">參數</span><span class="sxs-lookup"><span data-stu-id="4120b-111">PARAMETERS</span></span>

### <span data-ttu-id="4120b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4120b-112">-DefaultProfile</span></span>
<span data-ttu-id="4120b-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4120b-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4120b-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="4120b-114">-Name</span></span>
<span data-ttu-id="4120b-115">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="4120b-115">WebApp Name</span></span>

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

### <span data-ttu-id="4120b-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4120b-116">-ResourceGroupName</span></span>
<span data-ttu-id="4120b-117">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="4120b-117">Resource Group Name</span></span>

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

### <span data-ttu-id="4120b-118">-槽</span><span class="sxs-lookup"><span data-stu-id="4120b-118">-Slot</span></span>
<span data-ttu-id="4120b-119">槽名稱</span><span class="sxs-lookup"><span data-stu-id="4120b-119">Slot name</span></span>

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

### <span data-ttu-id="4120b-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="4120b-120">-WebApp</span></span>
<span data-ttu-id="4120b-121">管道 WebApp</span><span class="sxs-lookup"><span data-stu-id="4120b-121">Piped WebApp</span></span>

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

### <span data-ttu-id="4120b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4120b-122">CommonParameters</span></span>
<span data-ttu-id="4120b-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4120b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4120b-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4120b-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4120b-125">輸入</span><span class="sxs-lookup"><span data-stu-id="4120b-125">INPUTS</span></span>

### <span data-ttu-id="4120b-126">System.object</span><span class="sxs-lookup"><span data-stu-id="4120b-126">System.String</span></span>

### <span data-ttu-id="4120b-127">PSSite 中的 WebApps。</span><span class="sxs-lookup"><span data-stu-id="4120b-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="4120b-128">輸出</span><span class="sxs-lookup"><span data-stu-id="4120b-128">OUTPUTS</span></span>

### <span data-ttu-id="4120b-129">WebApps WebApps. AzureWebAppBackup （）</span><span class="sxs-lookup"><span data-stu-id="4120b-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="4120b-130">筆記</span><span class="sxs-lookup"><span data-stu-id="4120b-130">NOTES</span></span>

## <span data-ttu-id="4120b-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="4120b-131">RELATED LINKS</span></span>