---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 02396628-5E3E-49A6-8377-3F6DC488FEF8
online version: ''
schema: 2.0.0
ms.openlocfilehash: ee948161f101b83a4892441286b760a044e64358
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100405817"
---
# <span data-ttu-id="03660-101">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="03660-101">Get-AzureSiteRecoveryProtectionContainer</span></span>

## <span data-ttu-id="03660-102">簡介</span><span class="sxs-lookup"><span data-stu-id="03660-102">SYNOPSIS</span></span>
<span data-ttu-id="03660-103">為網站復原存放庫獲取保護容器。</span><span class="sxs-lookup"><span data-stu-id="03660-103">Gets protection containers for a Site Recovery vault.</span></span>

## <span data-ttu-id="03660-104">語法</span><span class="sxs-lookup"><span data-stu-id="03660-104">SYNTAX</span></span>

### <span data-ttu-id="03660-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="03660-105">Default (Default)</span></span>
```
Get-AzureSiteRecoveryProtectionContainer [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="03660-106">ById</span><span class="sxs-lookup"><span data-stu-id="03660-106">ById</span></span>
```
Get-AzureSiteRecoveryProtectionContainer -Id <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="03660-107">ByName</span><span class="sxs-lookup"><span data-stu-id="03660-107">ByName</span></span>
```
Get-AzureSiteRecoveryProtectionContainer -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="03660-108">描述</span><span class="sxs-lookup"><span data-stu-id="03660-108">DESCRIPTION</span></span>
<span data-ttu-id="03660-109">**Get-AzureSiteRecoveryProtectionContainer Cmdlet** 會取得目前 Azure 網站修復庫的保護容器。</span><span class="sxs-lookup"><span data-stu-id="03660-109">The **Get-AzureSiteRecoveryProtectionContainer** cmdlet gets protection containers for the current Azure Site Recovery vault.</span></span>
<span data-ttu-id="03660-110">保護容器是受保護物件的邏輯容器，例如虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="03660-110">A protection container is a logical container for protected objects such as virtual machines.</span></span>
<span data-ttu-id="03660-111">保護原則會定義受保護專案的複製設定，而且可以與保護容器相關聯，並適用于受保護的實體。</span><span class="sxs-lookup"><span data-stu-id="03660-111">Protection policies define replication settings for protected items and can be associated with a protection container and applied to a protected entity.</span></span>

## <span data-ttu-id="03660-112">例子</span><span class="sxs-lookup"><span data-stu-id="03660-112">EXAMPLES</span></span>

### <span data-ttu-id="03660-113">範例 1：取得受保護的容器</span><span class="sxs-lookup"><span data-stu-id="03660-113">Example 1: Get protected containers</span></span>
```
PS C:\> Get-AzureSiteRecoveryProtectionContainer
Name                        : PrimaryCloud
ID                          : fd00d920-79e4-4f2d-a282-a779c0cecb7f_ce995917-c962-45d0-b7f3-9f408a4e1429
FabricObjectId              : fd00d920-79e4-4f2d-a282-a779c0cecb7f
FabricType                  : VMM
Type                        : VMM
ServerId                    : fd00d920-79e4-4f2d-a282-a779c0cecb7f
Role                        : Primary
AvailableProtectionProfiles : {ab01dcbe-9da0-4c31-9564-d6904cfadfde, ad388147-83de-4d2f-a09d-fa46c626747e}
```

<span data-ttu-id="03660-114">此命令會為目前的儲存庫獲得受保護的容器。</span><span class="sxs-lookup"><span data-stu-id="03660-114">This command gets the protected containers for the current vault.</span></span>

## <span data-ttu-id="03660-115">參數</span><span class="sxs-lookup"><span data-stu-id="03660-115">PARAMETERS</span></span>

### <span data-ttu-id="03660-116">-Id</span><span class="sxs-lookup"><span data-stu-id="03660-116">-Id</span></span>
<span data-ttu-id="03660-117">指定要取得之受保護容器的識別碼。</span><span class="sxs-lookup"><span data-stu-id="03660-117">Specifies the ID of a protected container to get.</span></span>

```yaml
Type: String
Parameter Sets: ById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03660-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="03660-118">-Name</span></span>
<span data-ttu-id="03660-119">指定要取得的保護容器名稱。</span><span class="sxs-lookup"><span data-stu-id="03660-119">Specifies the name of a protection container to get.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03660-120">-設定檔</span><span class="sxs-lookup"><span data-stu-id="03660-120">-Profile</span></span>
<span data-ttu-id="03660-121">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="03660-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="03660-122">如果您未指定設定檔，此 Cmdlet 會從本地預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="03660-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03660-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03660-123">CommonParameters</span></span>
<span data-ttu-id="03660-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="03660-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03660-125">詳細資訊請參閱 https://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="03660-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03660-126">輸入</span><span class="sxs-lookup"><span data-stu-id="03660-126">INPUTS</span></span>

## <span data-ttu-id="03660-127">輸出</span><span class="sxs-lookup"><span data-stu-id="03660-127">OUTPUTS</span></span>

## <span data-ttu-id="03660-128">筆記</span><span class="sxs-lookup"><span data-stu-id="03660-128">NOTES</span></span>

## <span data-ttu-id="03660-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="03660-129">RELATED LINKS</span></span>




