---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.CloudService/new-azcloudserviceremotedesktopextensionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceRemoteDesktopExtensionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceRemoteDesktopExtensionObject.md
ms.openlocfilehash: 022093b8fe1df28a151405a18009b40dd24b0c97
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100138726"
---
# <span data-ttu-id="42a51-101">New-AzCloudServiceRemoteDesktopExtensionObject</span><span class="sxs-lookup"><span data-stu-id="42a51-101">New-AzCloudServiceRemoteDesktopExtensionObject</span></span>

## <span data-ttu-id="42a51-102">摘要</span><span class="sxs-lookup"><span data-stu-id="42a51-102">SYNOPSIS</span></span>
<span data-ttu-id="42a51-103">為遠端桌面延伸建立記憶體內建物件</span><span class="sxs-lookup"><span data-stu-id="42a51-103">Create a in-memory object for Remote Desktop Extension</span></span>

## <span data-ttu-id="42a51-104">句法</span><span class="sxs-lookup"><span data-stu-id="42a51-104">SYNTAX</span></span>

```
New-AzCloudServiceRemoteDesktopExtensionObject [-Name] <String> [-Credential] <PSCredential>
 [[-Expiration] <DateTime>] [[-TypeHandlerVersion] <String>] [[-RolesAppliedTo] <String[]>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [<CommonParameters>]
```

## <span data-ttu-id="42a51-105">說明</span><span class="sxs-lookup"><span data-stu-id="42a51-105">DESCRIPTION</span></span>
<span data-ttu-id="42a51-106">為遠端桌面延伸建立記憶體內建物件</span><span class="sxs-lookup"><span data-stu-id="42a51-106">Create a in-memory object for Remote Desktop Extension</span></span>

## <span data-ttu-id="42a51-107">示例</span><span class="sxs-lookup"><span data-stu-id="42a51-107">EXAMPLES</span></span>

### <span data-ttu-id="42a51-108">範例1：建立遠端桌面延伸物件</span><span class="sxs-lookup"><span data-stu-id="42a51-108">Example 1: Create remote desktop extension object</span></span>
```powershell
PS C:\> $credential = Get-Credential
PS C:\> $expiration = (Get-Date).AddYears(1)
PS C:\> $extension = New-AzCloudServiceRemoteDesktopExtensionObject -Name 'RDPExtension' -Credential $credential -Expiration $expiration -TypeHandlerVersion '1.2.1'
```

<span data-ttu-id="42a51-109">這個命令會建立用來建立或更新雲端服務的遠端桌面延伸物件。</span><span class="sxs-lookup"><span data-stu-id="42a51-109">This command creates remote desktop extension object which is used for creating or updating a cloud service.</span></span>
<span data-ttu-id="42a51-110">如需詳細資訊，請參閱新 AzCloudService。</span><span class="sxs-lookup"><span data-stu-id="42a51-110">For more details see New-AzCloudService.</span></span>

## <span data-ttu-id="42a51-111">參數</span><span class="sxs-lookup"><span data-stu-id="42a51-111">PARAMETERS</span></span>

### <span data-ttu-id="42a51-112">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="42a51-112">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="42a51-113">自動升級次要版本。</span><span class="sxs-lookup"><span data-stu-id="42a51-113">Auto upgrade minor version.</span></span>

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

### <span data-ttu-id="42a51-114">-認證</span><span class="sxs-lookup"><span data-stu-id="42a51-114">-Credential</span></span>
<span data-ttu-id="42a51-115">遠端桌面副檔名的認證。</span><span class="sxs-lookup"><span data-stu-id="42a51-115">Credential for Remote Desktop Extension.</span></span>

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

### <span data-ttu-id="42a51-116">-到期日</span><span class="sxs-lookup"><span data-stu-id="42a51-116">-Expiration</span></span>
<span data-ttu-id="42a51-117">遠端桌面延伸的到期時間。</span><span class="sxs-lookup"><span data-stu-id="42a51-117">Expiration for Remote Desktop Extension.</span></span>

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

### <span data-ttu-id="42a51-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="42a51-118">-Name</span></span>
<span data-ttu-id="42a51-119">遠端桌面副檔名的名稱。</span><span class="sxs-lookup"><span data-stu-id="42a51-119">Name of Remote Desktop Extension.</span></span>

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

### <span data-ttu-id="42a51-120">-RolesAppliedTo</span><span class="sxs-lookup"><span data-stu-id="42a51-120">-RolesAppliedTo</span></span>
<span data-ttu-id="42a51-121">已套用的角色。</span><span class="sxs-lookup"><span data-stu-id="42a51-121">Roles applied to.</span></span>

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

### <span data-ttu-id="42a51-122">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="42a51-122">-TypeHandlerVersion</span></span>
<span data-ttu-id="42a51-123">遠端桌面延伸版本。</span><span class="sxs-lookup"><span data-stu-id="42a51-123">Remote Desktop Extension version.</span></span>

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

### <span data-ttu-id="42a51-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42a51-124">CommonParameters</span></span>
<span data-ttu-id="42a51-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="42a51-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42a51-126">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="42a51-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42a51-127">輸入</span><span class="sxs-lookup"><span data-stu-id="42a51-127">INPUTS</span></span>

## <span data-ttu-id="42a51-128">輸出</span><span class="sxs-lookup"><span data-stu-id="42a51-128">OUTPUTS</span></span>

### <span data-ttu-id="42a51-129">Api20201001Preview. CloudService...。</span><span class="sxs-lookup"><span data-stu-id="42a51-129">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.Extension</span></span>

## <span data-ttu-id="42a51-130">筆記</span><span class="sxs-lookup"><span data-stu-id="42a51-130">NOTES</span></span>

<span data-ttu-id="42a51-131">別名</span><span class="sxs-lookup"><span data-stu-id="42a51-131">ALIASES</span></span>

## <span data-ttu-id="42a51-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="42a51-132">RELATED LINKS</span></span>

