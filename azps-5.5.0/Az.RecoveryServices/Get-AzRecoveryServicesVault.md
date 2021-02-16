---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 818B5302-91EE-425F-B1CD-86B626F1B7A3
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVault.md
ms.openlocfilehash: f667c0b13de510f7cf3e30e3faca9a93395ac221
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100135483"
---
# <span data-ttu-id="55ff2-101">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="55ff2-101">Get-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="55ff2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="55ff2-102">SYNOPSIS</span></span>

<span data-ttu-id="55ff2-103">取得恢復服務電子倉庫的清單。</span><span class="sxs-lookup"><span data-stu-id="55ff2-103">Gets a list of Recovery Services vaults.</span></span>

## <span data-ttu-id="55ff2-104">句法</span><span class="sxs-lookup"><span data-stu-id="55ff2-104">SYNTAX</span></span>

### <span data-ttu-id="55ff2-105">ByTagNameValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="55ff2-105">ByTagNameValueParameterSet</span></span>
```
Get-AzRecoveryServicesVault [[-ResourceGroupName] <String>] [[-Name] <String>] [-TagName <String>]
 [-TagValue <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="55ff2-106">ByTagObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="55ff2-106">ByTagObjectParameterSet</span></span>
```
Get-AzRecoveryServicesVault [[-ResourceGroupName] <String>] [[-Name] <String>] -Tag <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="55ff2-107">說明</span><span class="sxs-lookup"><span data-stu-id="55ff2-107">DESCRIPTION</span></span>

<span data-ttu-id="55ff2-108">**AzRecoveryServicesVault** Cmdlet 會在目前的訂閱中取得恢復服務電子倉庫的清單。</span><span class="sxs-lookup"><span data-stu-id="55ff2-108">The **Get-AzRecoveryServicesVault** cmdlet gets a list of Recovery Services vaults in the current subscription.</span></span>

## <span data-ttu-id="55ff2-109">示例</span><span class="sxs-lookup"><span data-stu-id="55ff2-109">EXAMPLES</span></span>

### <span data-ttu-id="55ff2-110">範例1</span><span class="sxs-lookup"><span data-stu-id="55ff2-110">Example 1</span></span>

```
PS C:\> Get-AzRecoveryServicesVault
```

<span data-ttu-id="55ff2-111">在選取的訂閱中取得保存庫清單。</span><span class="sxs-lookup"><span data-stu-id="55ff2-111">Get the list of vault in selected subscription.</span></span>

### <span data-ttu-id="55ff2-112">範例2</span><span class="sxs-lookup"><span data-stu-id="55ff2-112">Example 2</span></span>

```
PS C:\> Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup"
```

<span data-ttu-id="55ff2-113">在 [資源群組] 中取得選取訂閱的電子倉庫清單。</span><span class="sxs-lookup"><span data-stu-id="55ff2-113">Get the list of vault in resource group in selected subscription.</span></span>

### <span data-ttu-id="55ff2-114">範例3</span><span class="sxs-lookup"><span data-stu-id="55ff2-114">Example 3</span></span>

```
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $vault.Identity | fl

PrincipalId : XXXXXXXX-XXXX-XXXX
TenantId    : XXXXXXXX-XXXX-XXXX
Type        : SystemAssigned
```

<span data-ttu-id="55ff2-115">第一個 Cmdlet 會在資源群組中取得具有指定名稱的電子倉庫。</span><span class="sxs-lookup"><span data-stu-id="55ff2-115">The first cmdlet gets the vault in resource group with given name.</span></span> <span data-ttu-id="55ff2-116">接著我們從保存庫存取 MSI 資訊。</span><span class="sxs-lookup"><span data-stu-id="55ff2-116">Then we access the MSI information from the vault.</span></span>

## <span data-ttu-id="55ff2-117">參數</span><span class="sxs-lookup"><span data-stu-id="55ff2-117">PARAMETERS</span></span>

### <span data-ttu-id="55ff2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55ff2-118">-DefaultProfile</span></span>

<span data-ttu-id="55ff2-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="55ff2-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55ff2-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="55ff2-120">-Name</span></span>

<span data-ttu-id="55ff2-121">指定要查詢之保存庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="55ff2-121">Specifies the name of the vault to query for.</span></span>

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

### <span data-ttu-id="55ff2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55ff2-122">-ResourceGroupName</span></span>

<span data-ttu-id="55ff2-123">指定要從哪個 Azure 資源群組中檢索指定的復原服務物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="55ff2-123">Specifies the name of the Azure resource group from which to retrieve the specified Recovery Services object.</span></span>

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

### <span data-ttu-id="55ff2-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="55ff2-124">-Tag</span></span>

<span data-ttu-id="55ff2-125">指定要查詢的標記</span><span class="sxs-lookup"><span data-stu-id="55ff2-125">Specifies the Tags to query for</span></span>

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

### <span data-ttu-id="55ff2-126">-TagName</span><span class="sxs-lookup"><span data-stu-id="55ff2-126">-TagName</span></span>

<span data-ttu-id="55ff2-127">指定要查詢的標記的索引鍵</span><span class="sxs-lookup"><span data-stu-id="55ff2-127">Specifies the Key of the Tag to query for</span></span>

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

### <span data-ttu-id="55ff2-128">-TagValue</span><span class="sxs-lookup"><span data-stu-id="55ff2-128">-TagValue</span></span>

<span data-ttu-id="55ff2-129">指定要查詢的標記值</span><span class="sxs-lookup"><span data-stu-id="55ff2-129">Specifies the Value of the Tag to query for</span></span>

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

### <span data-ttu-id="55ff2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55ff2-130">CommonParameters</span></span>
<span data-ttu-id="55ff2-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="55ff2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55ff2-132">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="55ff2-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55ff2-133">輸入</span><span class="sxs-lookup"><span data-stu-id="55ff2-133">INPUTS</span></span>

### <span data-ttu-id="55ff2-134">所有</span><span class="sxs-lookup"><span data-stu-id="55ff2-134">None</span></span>

## <span data-ttu-id="55ff2-135">輸出</span><span class="sxs-lookup"><span data-stu-id="55ff2-135">OUTPUTS</span></span>

### <span data-ttu-id="55ff2-136">ARSVault 中的 RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="55ff2-136">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="55ff2-137">筆記</span><span class="sxs-lookup"><span data-stu-id="55ff2-137">NOTES</span></span>
<span data-ttu-id="55ff2-138">Get-AzRecoveryServicesVault 舊版本的 Az. RecoveryServices ( # B0 = 2.10.0) 無法與 Az 搭配使用。 ( # B1 = 1.8.1) 的帳戶不正確的程式集參照。</span><span class="sxs-lookup"><span data-stu-id="55ff2-138">Get-AzRecoveryServicesVault in old version of Az.RecoveryServices(<=2.10.0) cannot work with Az.Accounts(>=1.8.1) because of incorrect assembly reference.</span></span> <span data-ttu-id="55ff2-139">如果您使用的是最新的 Az 或 Az，RecoveryServices 需要升級至2.11.0 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="55ff2-139">The module Az.RecoveryServices needs to be upgraded to 2.11.0 or newer if you are using the latest Az or Az.Accounts.</span></span>

## <span data-ttu-id="55ff2-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="55ff2-140">RELATED LINKS</span></span>

[<span data-ttu-id="55ff2-141">AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="55ff2-141">Get-AzRecoveryServicesVaultSettingsFile</span></span>](./Get-AzRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="55ff2-142">新-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="55ff2-142">New-AzRecoveryServicesVault</span></span>](./New-AzRecoveryServicesVault.md)

[<span data-ttu-id="55ff2-143">移除-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="55ff2-143">Remove-AzRecoveryServicesVault</span></span>](./Remove-AzRecoveryServicesVault.md)
