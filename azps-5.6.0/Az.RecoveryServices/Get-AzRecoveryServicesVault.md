---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 818B5302-91EE-425F-B1CD-86B626F1B7A3
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVault.md
ms.openlocfilehash: a6aa52408cf1befd1c1208258c184be327ff2a15
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906893"
---
# <span data-ttu-id="599f3-101">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="599f3-101">Get-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="599f3-102">簡介</span><span class="sxs-lookup"><span data-stu-id="599f3-102">SYNOPSIS</span></span>

<span data-ttu-id="599f3-103">獲得復原服務庫清單。</span><span class="sxs-lookup"><span data-stu-id="599f3-103">Gets a list of Recovery Services vaults.</span></span>

## <span data-ttu-id="599f3-104">語法</span><span class="sxs-lookup"><span data-stu-id="599f3-104">SYNTAX</span></span>

### <span data-ttu-id="599f3-105">ByTagNameValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="599f3-105">ByTagNameValueParameterSet</span></span>
```
Get-AzRecoveryServicesVault [[-ResourceGroupName] <String>] [[-Name] <String>] [-TagName <String>]
 [-TagValue <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="599f3-106">ByTagObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="599f3-106">ByTagObjectParameterSet</span></span>
```
Get-AzRecoveryServicesVault [[-ResourceGroupName] <String>] [[-Name] <String>] -Tag <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="599f3-107">描述</span><span class="sxs-lookup"><span data-stu-id="599f3-107">DESCRIPTION</span></span>

<span data-ttu-id="599f3-108">**Get-AzRecoveryServicesVault** Cmdlet 會取得目前訂閱中的修復服務庫清單。</span><span class="sxs-lookup"><span data-stu-id="599f3-108">The **Get-AzRecoveryServicesVault** cmdlet gets a list of Recovery Services vaults in the current subscription.</span></span>

## <span data-ttu-id="599f3-109">例子</span><span class="sxs-lookup"><span data-stu-id="599f3-109">EXAMPLES</span></span>

### <span data-ttu-id="599f3-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="599f3-110">Example 1</span></span>

```
PS C:\> Get-AzRecoveryServicesVault
```

<span data-ttu-id="599f3-111">取得所選訂閱中的儲存庫清單。</span><span class="sxs-lookup"><span data-stu-id="599f3-111">Get the list of vault in selected subscription.</span></span>

### <span data-ttu-id="599f3-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="599f3-112">Example 2</span></span>

```
PS C:\> Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup"
```

<span data-ttu-id="599f3-113">取得所選訂閱中資源群組中的儲存庫清單。</span><span class="sxs-lookup"><span data-stu-id="599f3-113">Get the list of vault in resource group in selected subscription.</span></span>

### <span data-ttu-id="599f3-114">範例 3</span><span class="sxs-lookup"><span data-stu-id="599f3-114">Example 3</span></span>

```
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $vault.Identity | fl

PrincipalId : XXXXXXXX-XXXX-XXXX
TenantId    : XXXXXXXX-XXXX-XXXX
Type        : SystemAssigned
```

<span data-ttu-id="599f3-115">第一個 Cmdlet 會以指定名稱在資源群組中獲得該庫。</span><span class="sxs-lookup"><span data-stu-id="599f3-115">The first cmdlet gets the vault in resource group with given name.</span></span> <span data-ttu-id="599f3-116">然後，我們會從儲存庫存取 MSI 資訊。</span><span class="sxs-lookup"><span data-stu-id="599f3-116">Then we access the MSI information from the vault.</span></span>

## <span data-ttu-id="599f3-117">參數</span><span class="sxs-lookup"><span data-stu-id="599f3-117">PARAMETERS</span></span>

### <span data-ttu-id="599f3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="599f3-118">-DefaultProfile</span></span>

<span data-ttu-id="599f3-119">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="599f3-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="599f3-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="599f3-120">-Name</span></span>

<span data-ttu-id="599f3-121">指定要查詢的儲存庫名稱。</span><span class="sxs-lookup"><span data-stu-id="599f3-121">Specifies the name of the vault to query for.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="599f3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="599f3-122">-ResourceGroupName</span></span>

<span data-ttu-id="599f3-123">指定要從其中取回指定修復服務物件的 Azure 資源組名。</span><span class="sxs-lookup"><span data-stu-id="599f3-123">Specifies the name of the Azure resource group from which to retrieve the specified Recovery Services object.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="599f3-124">-標記</span><span class="sxs-lookup"><span data-stu-id="599f3-124">-Tag</span></span>

<span data-ttu-id="599f3-125">指定要查詢的標記</span><span class="sxs-lookup"><span data-stu-id="599f3-125">Specifies the Tags to query for</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByTagObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="599f3-126">-TagName</span><span class="sxs-lookup"><span data-stu-id="599f3-126">-TagName</span></span>

<span data-ttu-id="599f3-127">指定要查詢之標記的索引鍵</span><span class="sxs-lookup"><span data-stu-id="599f3-127">Specifies the Key of the Tag to query for</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="599f3-128">-TagValue</span><span class="sxs-lookup"><span data-stu-id="599f3-128">-TagValue</span></span>

<span data-ttu-id="599f3-129">指定要查詢的標記值</span><span class="sxs-lookup"><span data-stu-id="599f3-129">Specifies the Value of the Tag to query for</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="599f3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="599f3-130">CommonParameters</span></span>
<span data-ttu-id="599f3-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="599f3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="599f3-132">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="599f3-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="599f3-133">輸入</span><span class="sxs-lookup"><span data-stu-id="599f3-133">INPUTS</span></span>

### <span data-ttu-id="599f3-134">沒有</span><span class="sxs-lookup"><span data-stu-id="599f3-134">None</span></span>

## <span data-ttu-id="599f3-135">輸出</span><span class="sxs-lookup"><span data-stu-id="599f3-135">OUTPUTS</span></span>

### <span data-ttu-id="599f3-136">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="599f3-136">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="599f3-137">筆記</span><span class="sxs-lookup"><span data-stu-id="599f3-137">NOTES</span></span>
<span data-ttu-id="599f3-138">Get-AzRecoveryServicesVault版本的 Az.RecoveryServices (<=2.10.0) 無法使用 Az.Accounts (>=1.8.1) ，因為元件參照不正確。</span><span class="sxs-lookup"><span data-stu-id="599f3-138">Get-AzRecoveryServicesVault in old version of Az.RecoveryServices(<=2.10.0) cannot work with Az.Accounts(>=1.8.1) because of incorrect assembly reference.</span></span> <span data-ttu-id="599f3-139">如果您使用最新的 Az 或 Az.Accounts，模組 Az.RecoveryServices 必須升級至 2.11.0 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="599f3-139">The module Az.RecoveryServices needs to be upgraded to 2.11.0 or newer if you are using the latest Az or Az.Accounts.</span></span>

## <span data-ttu-id="599f3-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="599f3-140">RELATED LINKS</span></span>

[<span data-ttu-id="599f3-141">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="599f3-141">Get-AzRecoveryServicesVaultSettingsFile</span></span>](./Get-AzRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="599f3-142">New-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="599f3-142">New-AzRecoveryServicesVault</span></span>](./New-AzRecoveryServicesVault.md)

[<span data-ttu-id="599f3-143">Remove-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="599f3-143">Remove-AzRecoveryServicesVault</span></span>](./Remove-AzRecoveryServicesVault.md)
