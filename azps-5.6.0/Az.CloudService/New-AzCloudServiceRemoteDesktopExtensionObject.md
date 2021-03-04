---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.CloudService/new-azcloudserviceremotedesktopextensionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceRemoteDesktopExtensionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceRemoteDesktopExtensionObject.md
ms.openlocfilehash: 5ae7383f71524c87518b9f48cbb314bf74de633e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913970"
---
# <span data-ttu-id="49a09-101">New-AzCloudServiceRemoteDesktopExtensionObject</span><span class="sxs-lookup"><span data-stu-id="49a09-101">New-AzCloudServiceRemoteDesktopExtensionObject</span></span>

## <span data-ttu-id="49a09-102">簡介</span><span class="sxs-lookup"><span data-stu-id="49a09-102">SYNOPSIS</span></span>
<span data-ttu-id="49a09-103">建立遠端桌面擴充功能的記憶體內物件</span><span class="sxs-lookup"><span data-stu-id="49a09-103">Create a in-memory object for Remote Desktop Extension</span></span>

## <span data-ttu-id="49a09-104">語法</span><span class="sxs-lookup"><span data-stu-id="49a09-104">SYNTAX</span></span>

```
New-AzCloudServiceRemoteDesktopExtensionObject [-Name] <String> [-Credential] <PSCredential>
 [[-Expiration] <DateTime>] [[-TypeHandlerVersion] <String>] [[-RolesAppliedTo] <String[]>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [<CommonParameters>]
```

## <span data-ttu-id="49a09-105">描述</span><span class="sxs-lookup"><span data-stu-id="49a09-105">DESCRIPTION</span></span>
<span data-ttu-id="49a09-106">建立遠端桌面擴充功能的記憶體內物件</span><span class="sxs-lookup"><span data-stu-id="49a09-106">Create a in-memory object for Remote Desktop Extension</span></span>

## <span data-ttu-id="49a09-107">例子</span><span class="sxs-lookup"><span data-stu-id="49a09-107">EXAMPLES</span></span>

### <span data-ttu-id="49a09-108">範例 1：建立遠端桌面擴充物件</span><span class="sxs-lookup"><span data-stu-id="49a09-108">Example 1: Create remote desktop extension object</span></span>
```powershell
PS C:\> $credential = Get-Credential
PS C:\> $expiration = (Get-Date).AddYears(1)
PS C:\> $extension = New-AzCloudServiceRemoteDesktopExtensionObject -Name 'RDPExtension' -Credential $credential -Expiration $expiration -TypeHandlerVersion '1.2.1'
```

<span data-ttu-id="49a09-109">此命令會建立遠端桌面擴充物件，用來建立或更新雲端服務。</span><span class="sxs-lookup"><span data-stu-id="49a09-109">This command creates remote desktop extension object which is used for creating or updating a cloud service.</span></span>
<span data-ttu-id="49a09-110">詳情請參閱 New-AzCloudService。</span><span class="sxs-lookup"><span data-stu-id="49a09-110">For more details see New-AzCloudService.</span></span>

## <span data-ttu-id="49a09-111">參數</span><span class="sxs-lookup"><span data-stu-id="49a09-111">PARAMETERS</span></span>

### <span data-ttu-id="49a09-112">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="49a09-112">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="49a09-113">自動升級次要版本。</span><span class="sxs-lookup"><span data-stu-id="49a09-113">Auto upgrade minor version.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49a09-114">-認證</span><span class="sxs-lookup"><span data-stu-id="49a09-114">-Credential</span></span>
<span data-ttu-id="49a09-115">遠端桌面副檔名的認證。</span><span class="sxs-lookup"><span data-stu-id="49a09-115">Credential for Remote Desktop Extension.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49a09-116">-到期</span><span class="sxs-lookup"><span data-stu-id="49a09-116">-Expiration</span></span>
<span data-ttu-id="49a09-117">遠端桌面擴充功能到期。</span><span class="sxs-lookup"><span data-stu-id="49a09-117">Expiration for Remote Desktop Extension.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49a09-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="49a09-118">-Name</span></span>
<span data-ttu-id="49a09-119">遠端桌面副檔名的名稱。</span><span class="sxs-lookup"><span data-stu-id="49a09-119">Name of Remote Desktop Extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49a09-120">-RolesAppliedTo</span><span class="sxs-lookup"><span data-stu-id="49a09-120">-RolesAppliedTo</span></span>
<span data-ttu-id="49a09-121">角色。</span><span class="sxs-lookup"><span data-stu-id="49a09-121">Roles applied to.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49a09-122">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="49a09-122">-TypeHandlerVersion</span></span>
<span data-ttu-id="49a09-123">遠端桌面擴充功能版本。</span><span class="sxs-lookup"><span data-stu-id="49a09-123">Remote Desktop Extension version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49a09-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49a09-124">CommonParameters</span></span>
<span data-ttu-id="49a09-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="49a09-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49a09-126">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="49a09-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49a09-127">輸入</span><span class="sxs-lookup"><span data-stu-id="49a09-127">INPUTS</span></span>

## <span data-ttu-id="49a09-128">輸出</span><span class="sxs-lookup"><span data-stu-id="49a09-128">OUTPUTS</span></span>

### <span data-ttu-id="49a09-129">Microsoft.Azure.PowerShell.Cmdlets.CloudService.models.Api20201001Preview.extension</span><span class="sxs-lookup"><span data-stu-id="49a09-129">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.Extension</span></span>

## <span data-ttu-id="49a09-130">筆記</span><span class="sxs-lookup"><span data-stu-id="49a09-130">NOTES</span></span>

<span data-ttu-id="49a09-131">別名</span><span class="sxs-lookup"><span data-stu-id="49a09-131">ALIASES</span></span>

## <span data-ttu-id="49a09-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="49a09-132">RELATED LINKS</span></span>

