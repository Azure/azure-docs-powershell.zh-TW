---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 02396628-5E3E-49A6-8377-3F6DC488FEF8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 75a083c2f892b7b4f07c37ef978d1babb1dd0cb0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967039"
---
# <span data-ttu-id="c1a97-101">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="c1a97-101">Get-AzureSiteRecoveryProtectionContainer</span></span>

## <span data-ttu-id="c1a97-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c1a97-102">SYNOPSIS</span></span>
<span data-ttu-id="c1a97-103">取得網站恢復電子倉庫的保護容器。</span><span class="sxs-lookup"><span data-stu-id="c1a97-103">Gets protection containers for a Site Recovery vault.</span></span>

## <span data-ttu-id="c1a97-104">句法</span><span class="sxs-lookup"><span data-stu-id="c1a97-104">SYNTAX</span></span>

### <span data-ttu-id="c1a97-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="c1a97-105">Default (Default)</span></span>
```
Get-AzureSiteRecoveryProtectionContainer [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="c1a97-106">ById</span><span class="sxs-lookup"><span data-stu-id="c1a97-106">ById</span></span>
```
Get-AzureSiteRecoveryProtectionContainer -Id <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="c1a97-107">ByName</span><span class="sxs-lookup"><span data-stu-id="c1a97-107">ByName</span></span>
```
Get-AzureSiteRecoveryProtectionContainer -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c1a97-108">說明</span><span class="sxs-lookup"><span data-stu-id="c1a97-108">DESCRIPTION</span></span>
<span data-ttu-id="c1a97-109">**AzureSiteRecoveryProtectionContainer** Cmdlet 會取得目前 Azure Site Recovery 保存庫的保護容器。</span><span class="sxs-lookup"><span data-stu-id="c1a97-109">The **Get-AzureSiteRecoveryProtectionContainer** cmdlet gets protection containers for the current Azure Site Recovery vault.</span></span>
<span data-ttu-id="c1a97-110">保護容器是受保護物件（例如虛擬電腦）的邏輯容器。</span><span class="sxs-lookup"><span data-stu-id="c1a97-110">A protection container is a logical container for protected objects such as virtual machines.</span></span>
<span data-ttu-id="c1a97-111">保護原則定義受保護專案的複製設定，而且可以與保護容器相關聯，並套用到受保護的實體。</span><span class="sxs-lookup"><span data-stu-id="c1a97-111">Protection policies define replication settings for protected items and can be associated with a protection container and applied to a protected entity.</span></span>

## <span data-ttu-id="c1a97-112">示例</span><span class="sxs-lookup"><span data-stu-id="c1a97-112">EXAMPLES</span></span>

### <span data-ttu-id="c1a97-113">範例1：取得受保護的容器</span><span class="sxs-lookup"><span data-stu-id="c1a97-113">Example 1: Get protected containers</span></span>
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

<span data-ttu-id="c1a97-114">這個命令會取得目前電子倉庫中受保護的容器。</span><span class="sxs-lookup"><span data-stu-id="c1a97-114">This command gets the protected containers for the current vault.</span></span>

## <span data-ttu-id="c1a97-115">參數</span><span class="sxs-lookup"><span data-stu-id="c1a97-115">PARAMETERS</span></span>

### <span data-ttu-id="c1a97-116">-識別碼</span><span class="sxs-lookup"><span data-stu-id="c1a97-116">-Id</span></span>
<span data-ttu-id="c1a97-117">指定要取得之受保護容器的識別碼。</span><span class="sxs-lookup"><span data-stu-id="c1a97-117">Specifies the ID of a protected container to get.</span></span>

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

### <span data-ttu-id="c1a97-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="c1a97-118">-Name</span></span>
<span data-ttu-id="c1a97-119">指定要取得的保護容器的名稱。</span><span class="sxs-lookup"><span data-stu-id="c1a97-119">Specifies the name of a protection container to get.</span></span>

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

### <span data-ttu-id="c1a97-120">-設定檔</span><span class="sxs-lookup"><span data-stu-id="c1a97-120">-Profile</span></span>
<span data-ttu-id="c1a97-121">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="c1a97-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c1a97-122">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="c1a97-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c1a97-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1a97-123">CommonParameters</span></span>
<span data-ttu-id="c1a97-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c1a97-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1a97-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c1a97-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1a97-126">輸入</span><span class="sxs-lookup"><span data-stu-id="c1a97-126">INPUTS</span></span>

## <span data-ttu-id="c1a97-127">輸出</span><span class="sxs-lookup"><span data-stu-id="c1a97-127">OUTPUTS</span></span>

## <span data-ttu-id="c1a97-128">筆記</span><span class="sxs-lookup"><span data-stu-id="c1a97-128">NOTES</span></span>

## <span data-ttu-id="c1a97-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="c1a97-129">RELATED LINKS</span></span>

[<span data-ttu-id="c1a97-130">Azure Site Recovery 服務 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c1a97-130">Azure Site Recovery Services Cmdlets</span></span>](./Azure.SiteRecoveryServices.md)


